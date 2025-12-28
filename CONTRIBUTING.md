# Contributing Guidelines

We welcome contributions to improve this .gitignores template collection. This document outlines the process and standards for contributing new templates or improving existing ones.

For comprehensive project information, refer to:
- [README.md](README.md) - User documentation and overview
- [AGENTS.md](AGENTS.md) - Maintainer documentation and detailed standards

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Types of Contributions](#types-of-contributions)
- [Template Guidelines](#template-guidelines)
- [Testing Your Template](#testing-your-template)
- [Submission Process](#submission-process)
- [Review Process](#review-process)
- [Quality Assurance Checklist](#quality-assurance-checklist)
- [Maintenance and Updates](#maintenance-and-updates)
- [Getting Help](#getting-help)

## Code of Conduct

We are committed to providing a friendly, safe, and welcoming environment for all contributors. By participating in this project, you agree to:

- Be respectful and inclusive in your language and actions
- Focus on what is best for the community and project
- Provide constructive feedback and accept it gracefully
- Show empathy towards other community members

Unacceptable behavior includes, but is not limited to:

- Any conduct that could reasonably be considered inappropriate in a professional setting
- Harassment, discrimination, or personal attacks
- Publishing others' private information without permission
- Trolling, insulting, or derogatory comments

## Getting Started

### Prerequisites

- Basic understanding of the programming language or framework you're creating a template for
- Familiarity with Git and `.gitignore` syntax
- Git and GitHub account

### Setting Up Your Development Environment

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/.gitignores.git
   cd .gitignores
   ```
3. **Create a new branch** for your contribution:
   ```bash
   git checkout -b feature/new-template-name
   ```

### Project Structure

For detailed project structure information, refer to the [Project Structure Reference](AGENTS.md#project-structure-reference) or the [Folder Structure](README.md#folder-structure) section in the README.

## Types of Contributions

We welcome several types of contributions:

1. **New Templates**: Create templates for new languages, frameworks, or tools
2. **Template Improvements**: Update existing templates with better patterns or organization
3. **Bug Fixes**: Correct errors in existing templates
4. **Documentation**: Improve README, CONTRIBUTING.md, or other documentation
5. **Testing**: Test templates with real projects and report issues

## Template Guidelines

### File Naming Convention

All template files use URL-friendly naming conventions based on official technology names. Follow these rules consistently:

#### Basic Principles

- **Official Names**: Use the official technology name as the basis for the file name
- **Lowercase**: All file names must be lowercase
- **URL-Friendly**: Convert names to be URL-friendly (no spaces, special characters)
- **Readability**: Optimize for readability while maintaining consistency

#### Decision Rules: Hyphen (-) vs Underscore (_)

Use the following rules to determine which separator to use:

1. **Use Hyphens (-) when:**
   - The technology name contains **spaces** (e.g., "React Native" → `react-native.gitignore`)
   - The technology name is a **multi-word name without special characters** (e.g., "Spring Boot" → `spring-boot.gitignore`)

2. **Use Underscores (_) when:**
   - The technology name contains a **dot (.)** that needs replacement (e.g., "Next.js" → `next_js.gitignore`, "Vue.js" → `vue_js.gitignore`)
   - The technology name contains **special characters** (e.g., "C#" → `c_sharp.gitignore`, ".NET" → `dot_net.gitignore`)
   - The official name has **"JS" as a distinct suffix** in the branding (e.g., "AdonisJS" → `adonis_js.gitignore`)
   - When the technology name is a **branded single word** even if it contains multiple parts (e.g., "NestJS" → `nest_js.gitignore`, "SvelteKit" → `svelte_kit.gitignore`)

3. **No Separator (single word):**
   - When the technology name is a **single word** (e.g., "React" → `react.gitignore`)

### Template Structure

All templates should follow the structure demonstrated in the reference template `reference_template.gitignore`. Use this template as the definitive source of truth when creating or updating templates.

**Key Principles:**
- **Follow reference_template**: All templates should match the structure, organization, and security approach shown in `reference_template.gitignore`
- **Security-first**: Always place security patterns first for maximum protection
- **Comprehensive coverage**: Include patterns for all relevant technology categories
- **Organized structure**: Use logical grouping with descriptive headers
- **Alphabetical sorting**: Sort patterns alphabetically within each section (case-insensitive)
- **Template type clarity**: Use appropriate template type in header (Framework, Language, Tool, IDE, OS, Platform, Common)

For detailed structure examples, template type classification, and practical creation examples, refer to the comprehensive guidance in `reference_template.gitignore`.

### Content Guidelines

#### 1. Check Official Sources First

**CRITICAL**: Before creating or updating templates, always check for and use official `.gitignore` files from the technology's official repositories whenever they exist. This ensures:

- **Accuracy**: Official repositories contain the most up-to-date and accurate ignore patterns
- **Best Practices**: Patterns reflect the technology's recommended practices
- **Completeness**: Official templates include all framework/tool-specific artifacts
- **Community Alignment**: Maintains consistency with the broader developer community

**Sources for Official .gitignore Files:**
1. **GitHub Official Repositories**: Most frameworks and tools maintain official `.gitignore` files
2. **GitHub's official gitignore repository**: [github/gitignore](https://github.com/github/gitignore)
3. **Project Documentation**: Some projects include `.gitignore` recommendations
4. **Starter Templates**: Official starter templates often include optimal `.gitignore` files

#### 2. Pattern Selection Criteria

Include patterns that:
- **Significantly impact repository performance** (large directories, cache files)
- **Improve security** (sensitive files, credentials)
- **Are commonly excluded** in production projects
- **Are specific to the technology** (not generic patterns)

Exclude patterns that:
- **Are already covered** by other templates you might combine with
- **Are too specific** to individual development workflows
- **Might exclude essential files** needed for the project

#### 3. Pattern Syntax
- Use `**/` prefix for directories to match at any depth
- Use `*` for wildcard matching
- Use `!` for negation (use sparingly and document clearly)
- Use `#` for comments to explain non-obvious patterns

#### 4. Framework vs Language Templates
- **Framework Templates**: Should be comprehensive and self-contained with everything needed for that specific framework, including framework-specific patterns and relevant security patterns (e.g., `.env*` files)
- **Language Templates**: Should contain only language-specific patterns and should be combined with framework templates when needed

### Template Development Process

1. **Research**: Identify common patterns for the technology
2. **Structure**: Organize into logical categories
3. **Formatting**: Follow naming conventions and template structure
4. **Testing**: Validate with sample projects using Git commands
5. **Documentation**: Add combination instructions in template header

## Testing Your Template

### Basic Validation

Test your template with a sample project:

```bash
# Create a test directory
mkdir test-project && cd test-project

# Copy your template
cp ../path/to/your/template.gitignore .gitignore

# Create some test files that should be excluded
touch .env node_modules/package.json dist/bundle.js

# Test Git status
git init
git status
```

### Pattern Testing

Verify that:

1. **Excluded patterns work correctly**: Files matching patterns are not tracked by Git
2. **Essential files are included**: Files needed for the project are not accidentally excluded
3. **Patterns don't conflict**: No unintended pattern interactions

### Integration Testing

Test template combinations:

```bash
# Test combining multiple templates
cat language-template.gitignore \
    framework-template.gitignore \
    common/security.gitignore > .gitignore

# Verify no duplicate patterns
cat template1 template2 | sort -u | wc -l
```

### Edge Cases

Test with:
- Nested directories
- Pattern negation (`!`)
- Wildcard patterns
- Different Git versions

## Template Development Guidelines

### Creating New Templates

1. **Research Phase**
   - Study existing templates to understand the pattern structure
   - Research common patterns for the technology
   - **Always check for official `.gitignore` files from the technology's official repositories**
   - Check official documentation for recommended ignore patterns
   - Review community resources and best practices

2. **Categorization**
   - Determine the appropriate category directory based on technology type
   - Place template in correct directory: `languages/`, `frameworks/`, `tools/`, `platforms/`, `os/`, or `ides/`
   - Consider if the template should be global or project-specific

3. **Structure Implementation**
   - Include header comment with gitignores.com reference
   - Add section comments to group related patterns with visual separators
   - Sort patterns alphabetically within each section
   - Include explanatory comments for complex or non-obvious patterns

4. **Testing and Validation**
   - Test template in isolation to verify it works correctly
   - Test template combinations (e.g., language + editor templates)
   - Verify patterns don't exclude necessary files
   - Test with common edge cases and special characters

5. **Documentation**
   - Update README.md to include new template in appropriate section
   - Add template to AGENTS.md documentation if significant
   - Ensure documentation accurately describes the template's purpose

### Updating Existing Templates

1. **Review Process**
   - Check for outdated patterns or missing common patterns
   - Review community feedback and issues
   - Check for changes in the technology that might affect patterns
   - Identify duplicate or conflicting patterns

2. **Implementation**
   - Ensure updates don't break existing functionality
   - Maintain alphabetical sorting and comment structure
   - Test changes thoroughly before submission
   - Consider backward compatibility for existing users

3. **Documentation Updates**
   - Note significant changes in commit messages
   - Update documentation if patterns significantly change
   - Document deprecation of old patterns if applicable

## Submission Process

1. **Fork repository**: Create your own fork of the repository
2. **Create feature branch**: Use a descriptive branch name (e.g., `add-rust-template` or `fix-python-patterns`)
3. **Add template to correct category**: Place your template in the appropriate directory
4. **Test template functionality**: Verify the template works correctly with Git
5. **Update documentation**: If adding a new template, update README.md to include it in the appropriate section
6. **Submit pull request**: Provide a clear description of your changes

## Quality Standards

### Official Source Priority

When creating or updating templates, **always prioritize using official `.gitignore` files** from the technology's official repositories. This ensures:

1. **Accuracy**: Official repositories contain the most up-to-date and accurate ignore patterns
2. **Best Practices**: Patterns reflect the technology's recommended practices
3. **Completeness**: Official templates include all framework/tool-specific artifacts
4. **Community Alignment**: Maintains consistency with the broader developer community

**Key sources for official `.gitignore` files:**
- GitHub official repositories of frameworks and tools
- GitHub's official [github/gitignore](https://github.com/github/gitignore) repository
- Project documentation and official starter templates
- Official starter templates (e.g., `create-react-app`, `vue create`)

**Verification process when using official sources:**
1. Include a comment with the source repository URL
2. Verify patterns work correctly with Git syntax
3. Cross-reference with common patterns in the `common/` directory
4. Test patterns with sample projects to ensure they work as expected

### Template Validation Checklist

#### Syntax Validation
- [ ] Verify all patterns follow Git ignore syntax rules
- [ ] Check for proper use of wildcards and patterns
- [ ] Validate directory vs file pattern syntax
- [ ] Test pattern negation syntax if used

#### Content Validation
- [ ] Check for duplicate patterns within the template
- [ ] Verify patterns are sorted alphabetically within sections
- [ ] Ensure section comments are descriptive and accurate
- [ ] Validate that patterns don't conflict with each other

#### Naming and Structure Validation
- [ ] Confirm file name follows project standards
- [ ] Verify template is in correct category directory
- [ ] Check header comment includes gitignores.com reference
- [ ] Validate file encoding and line endings

#### Integration Testing
- [ ] Test template in isolation with Git
- [ ] Test template combinations with related templates
- [ ] Verify patterns work across different operating systems
- [ ] Test edge cases and special characters

### Review Process
- All contributions will be reviewed for adherence to project standards
- Templates must meet quality standards before merging
- Feedback will be provided for improvements if needed
- Documentation must be updated to reflect new or modified templates

## Quality Assurance Checklist

Before submitting, verify your template meets these quality standards:

### ✅ File Structure

- [ ] Correct file name following naming conventions
- [ ] Template in correct directory (`languages/`, `frameworks/`, etc.)
- [ ] Standard header format with proper template type
- [ ] Clear usage notes and combination instructions

### ✅ Pattern Quality

- [ ] Patterns sorted alphabetically within categories
- [ ] Logical category organization with clear headers
- [ ] No duplicate patterns within the template
- [ ] Appropriate pattern selection (not too broad, not too specific)
- [ ] Security-sensitive patterns included (`.env*`, credentials, etc.)

### ✅ Technical Accuracy

- [ ] Patterns use correct Git ignore syntax
- [ ] No syntax errors or malformed patterns
- [ ] Patterns tested with real Git commands
- [ ] Essential files not accidentally excluded

### ✅ Documentation

- [ ] Clear comments explaining non-obvious patterns
- [ ] References to official sources (if used)
- [ ] Combination guidance with other templates
- [ ] Warnings about pattern conflicts or duplication

### ✅ Testing

- [ ] Basic validation with `git status`
- [ ] Pattern testing with sample files
- [ ] Integration testing with template combinations
- [ ] Edge case testing (nested directories, wildcards, etc.)

## Maintenance and Updates

### Template Updates

When updating existing templates:

1. **Check for official updates**: Verify if the technology has updated its official `.gitignore` recommendations
2. **Review community feedback**: Consider issues and pull requests related to the template
3. **Test thoroughly**: Ensure updates don't break existing functionality
4. **Document changes**: Update comments and documentation as needed

### Deprecation Policy

Templates may be deprecated if:
- The technology is no longer maintained or widely used
- Better alternatives exist
- The template contains outdated or incorrect patterns

Deprecated templates will be:
1. Moved to an archive directory
2. Clearly marked as deprecated
3. Removed from the main directories after a reasonable period

## Getting Help

If you need help or have questions about contributing:
- Check existing templates for examples
- Review the AGENTS.md file for detailed project information
- Open an issue for discussion before implementing major changes
- Refer to [gitignores.com](https://gitignores.com) for additional guidance
