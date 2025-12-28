# Contributing Guidelines

We welcome contributions to improve this gitignore template collection. This document outlines the process and standards for contributing new templates or improving existing ones.

For a comprehensive project overview and detailed information, please refer to [README.md](README.md) for user documentation and [AGENTS.md](AGENTS.md) for maintainer documentation.

**Current Repository Statistics (January 2026):**

- **Total Templates**: 124 gitignore files (including root `.gitignore`)
- **Common Patterns**: 8 templates in `common/` directory with enhanced organization
- **Language Templates**: 28 templates in `languages/` directory
- **Framework Templates**: 30 templates in `frameworks/` directory
- **Tool Templates**: 37 templates in `tools/` directory
- **Editor Templates**: 14 templates in `ides/` directory
- **Operating System Templates**: 3 templates in `os/` directory
- **Platform Templates**: 3 templates in `platforms/` directory

## Template Requirements

### File Structure Standards

- All `.gitignore` template files must include `# Template from gitignores.com - Online .gitignore generator` as the first line
- Patterns within each `.gitignore` file must be sorted alphabetically within sections
- Use section comments to group related patterns with clear visual separators
- Maintain consistent indentation and spacing throughout the file
- Remove trailing whitespace from all lines
- Limit empty lines to 0-1 at the end of files

### Enhanced Standard Template Structure

All templates should follow this enhanced organizational structure:

1. **Header Section**
   - Source attribution: `# Template from gitignores.com - Online .gitignore generator`
   - Technology name and brief description
   - Clear section organization with visual separators

2. **Technology-Specific Patterns**
   - Organized into logical categories with clear headers using visual separators
   - Patterns sorted alphabetically within each category
   - Comprehensive coverage of technology-specific artifacts
   - Descriptive comments explaining pattern purposes

3. **Common Patterns Reference**
   - References to relevant common patterns in the `common/` directory
   - Examples of how to combine templates with common patterns
   - Clear guidance on comprehensive coverage
   - Best practices for template combination

4. **Official Sources**
   - Links to official GitHub repositories or documentation
   - Attribution for patterns based on official sources
   - References to community best practices

5. **Usage Notes**
   - Important usage information and considerations
   - Recommendations for production projects
   - Guidance on customization and best practices
   - Security considerations and warnings

**Visual Separators:**
- Use `# ============================================================================` for major section breaks
- Use `# ----------------------------------------------------------------------------` for category headers
- Use `# ` for regular comments and descriptions

### File Naming Standards

- File names must use lowercase for consistency
- Use underscores or hyphens for multi-word names as appropriate (e.g., `vscode.gitignore`, `next_js.gitignore`)
- Avoid spaces and special characters in file names
- File names should be URL-friendly and descriptive
- Follow existing naming conventions in the repository

### Content Standards

- Provide clear, concise rules that follow Git ignore syntax
- Include relevant comments explaining why patterns are included
- Test templates work correctly with Git before submission
- Follow existing pattern conventions and structure
- Avoid duplicate patterns within the same template
- Escape spaces in patterns with single backslash (e.g., `Package\\ Control.cache`)
- Ensure patterns are properly sorted alphabetically within sections

### Documentation Standards

- Documentation must reference file names exactly as they exist in the repository
- Lists in markdown files must be sorted alphabetically
- All documentation files must be consistent with each other
- README.md should accurately reflect available templates and their locations
- Keep documentation up-to-date with template changes

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
   - Place template in correct directory: `languages/`, `frameworks/`, `tools/`, `platforms/`, `operating-systems/`, or `editors/`
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

## Getting Help

If you need help or have questions about contributing:

- Check existing templates for examples
- Review the AGENTS.md file for detailed project information
- Open an issue for discussion before implementing major changes
- Refer to [gitignores.com](https://gitignores.com) for additional guidance
- Review the comprehensive handover document in AGENTS.md for detailed project standards and procedures
