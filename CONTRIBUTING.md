# Contributing to .gitignores Templates Collection

Thank you for your interest in contributing to the .gitignores Templates Collection! This repository contains **129 standardized `.gitignore` templates** for programming languages, frameworks, tools, and development environments.

**Online Reference**: [gitignores.com](https://gitignores.com) – Online .gitignore generator and template reference

## 📋 Quick Navigation

- [📜 Code of Conduct](#-code-of-conduct)
- [🚀 Getting Started](#-getting-started)
- [📝 Types of Contributions](#-types-of-contributions)
- [📚 Template Standards Reference](#-template-standards-reference)
- [🔧 Template Development Process](#-template-development-process)
- [🧪 Testing Your Template](#-testing-your-template)
- [📤 Submission Process](#-submission-process)
- [✅ Quality Standards](#-quality-standards)
- [🔄 Maintenance and Updates](#-maintenance-and-updates)
- [❓ Getting Help](#-getting-help)

## 📜 Code of Conduct

Please follow our community guidelines to ensure a welcoming and respectful environment for all contributors.

## 🚀 Getting Started

### Prerequisites

- Basic understanding of the programming language or framework you're creating a template for
- Familiarity with Git and `.gitignore` syntax
- Git and GitHub account

### First-Time Setup

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

## 📝 Types of Contributions

We welcome several types of contributions:

| Type                      | Description                                                    | Examples                                              |
| ------------------------- | -------------------------------------------------------------- | ----------------------------------------------------- |
| **New Templates**         | Create templates for new languages, frameworks, or tools       | `rust.gitignore`, `svelte.gitignore`, `bun.gitignore` |
| **Template Improvements** | Update existing templates with better patterns or organization | Add missing patterns, improve organization            |
| **Bug Fixes**             | Correct errors in existing templates                           | Fix syntax errors, remove incorrect patterns          |
| **Documentation**         | Improve README, CONTRIBUTING.md, or other documentation        | Add examples, improve clarity                         |
| **Testing**               | Test templates with real projects and report issues            | Verify patterns work correctly                        |

## 📚 Template Standards Reference

**IMPORTANT**: All templates must follow the standards defined in [`TEMPLATE_STANDARDS.md`](TEMPLATE_STANDARDS.md). This file serves as the definitive source of truth for all template creation and maintenance standards.

**DO NOT** summarize or duplicate standards here. Instead, thoroughly review and follow `TEMPLATE_STANDARDS.md` exactly when creating or updating templates.

## 🔧 Template Development Process

### Creating New Templates

#### 1. Research Phase

- Study existing templates to understand the pattern structure
- Research common patterns for the technology
- Check for official `.gitignore` files from the technology's repository
- Review similar technologies in the collection for reference

#### 2. Template Creation

- Use `TEMPLATE_STANDARDS.md` as your starting point
- Follow the exact structure and formatting standards
- Include proper attribution and template type declarations
- Add comprehensive usage notes and combination guidance

#### 3. Pattern Selection

- Include patterns that significantly impact repository performance
- Add security patterns for framework templates
- Focus on technology-specific artifacts
- Avoid overly broad patterns that might exclude essential files

### Updating Existing Templates

1. **Check for Official Updates**: Verify if the technology has updated its official `.gitignore` recommendations
2. **Review Community Feedback**: Check GitHub issues for reported problems or suggestions
3. **Test Changes**: Verify updates work correctly with sample projects
4. **Maintain Backward Compatibility**: Ensure updates don't break existing usage

## 🧪 Testing Your Template

For comprehensive testing procedures and validation commands, refer to the [Template Testing & Validation section in TEMPLATE_STANDARDS.md](TEMPLATE_STANDARDS.md#9-template-testing--validation). This includes detailed testing commands, validation scripts, and best practices.

### Basic Validation

Test your template with a sample project:

```bash
# Create a test directory
mkdir test-project && cd test-project

# Copy your template
cp ../path/to/your/template.gitignore .gitignore

# Initialize git repository
git init

# Test with sample files
touch .env config.json build/ dist/ node_modules/

# Check what's ignored
git status --ignored
```

### Manual Validation

Since validation scripts are not currently available, manually validate your template:

1. **Check for duplicate patterns**: Use `grep` to identify duplicate lines
2. **Verify alphabetical sorting**: Ensure patterns are sorted alphabetically within sections
3. **Test with Git commands**: Use `git status --ignored` and `git check-ignore -v <file>`
4. **Review against standards**: Compare your template with `TEMPLATE_STANDARDS.md` requirements

## 📤 Submission Process

### Step-by-Step Guide

1. **Fork repository**: Create your own fork of the repository
2. **Create feature branch**: Use a descriptive branch name (e.g., `add-rust-template` or `fix-python-patterns`)
3. **Make changes**: Follow the template standards and development guidelines
4. **Test thoroughly**: Verify your template works correctly
5. **Commit changes**: Use descriptive commit messages
6. **Push to your fork**: `git push origin feature-branch-name`
7. **Create pull request**: Submit PR with clear description of changes

### Pull Request Requirements

- **Descriptive title**: Clearly state what the PR does
- **Detailed description**: Explain the changes and their purpose
- **Testing information**: Describe how you tested the template
- **References**: Link to official sources or related issues
- **Checklist**: Confirm all quality standards are met

### Example PR Description

```markdown
## Summary

Adds new template for Rust programming language

## Changes

- Created `languages/rust.gitignore` with Rust-specific patterns
- Includes common Rust artifacts: `target/`, `Cargo.lock`, etc.
- Follows TEMPLATE_STANDARDS.md structure

## Testing

- Tested with sample Rust project
- Verified patterns work with `git check-ignore`
- Checked for duplicate patterns

## References

- Official Rust .gitignore: https://github.com/rust-lang/rust/blob/master/.gitignore
- Issue #123: Request for Rust template
```

## ✅ Quality Standards

### Official Source Priority

When creating or updating templates, **always prioritize using official `.gitignore` files** from the technology's official repositories. This ensures:

- **Accuracy**: Official repositories contain the most up-to-date and accurate ignore patterns
- **Best Practices**: Patterns reflect the technology's recommended practices
- **Completeness**: Official templates include all framework/tool-specific artifacts
- **Community Alignment**: Maintains consistency with the broader developer community

### Sources for Official .gitignore Files

1. **GitHub Official Repositories**: Most frameworks and tools maintain official `.gitignore` files
2. **Project Documentation**: Some projects include `.gitignore` recommendations
3. **Starter Templates**: Official starter templates often include optimal `.gitignore` files

### Quality Assurance Checklist

For the complete quality assurance checklist and validation standards, refer to the [Template Validation Checklist section in TEMPLATE_STANDARDS.md](TEMPLATE_STANDARDS.md#7-template-validation-checklist). This includes:

- **File Structure Requirements**: Correct naming, directory placement, header format
- **Pattern Quality Standards**: Alphabetical sorting, logical organization, no duplicates
- **Technical Accuracy**: Correct Git syntax, tested patterns, no false positives
- **Documentation Requirements**: Clear comments, references, combination guidance

## 🔄 Maintenance and Updates

### Template Updates

When updating existing templates:

1. **Check for official updates**: Verify if the technology has updated its official `.gitignore` recommendations
2. **Review community feedback**: Check GitHub issues for reported problems or suggestions
3. **Test changes**: Verify updates work correctly with sample projects
4. **Maintain backward compatibility**: Ensure updates don't break existing usage

### Regular Maintenance Schedule

- **Quarterly Review**: Review all templates every 3 months for outdated patterns
- **Annual Audit**: Comprehensive review of all templates annually
- **Technology Updates**: Update templates when new versions of technologies are released
- **Pattern Optimization**: Continuously optimize patterns for better performance and accuracy

### Community Feedback

We value community feedback and contributions:

- **Report Issues**: Use GitHub Issues to report problems or suggest improvements
- **Discuss Changes**: Use GitHub Discussions for larger changes or new template proposals
- **Share Experiences**: Let us know how you're using the templates in your projects

## ❓ Getting Help

If you need help or have questions:

1. **Check Documentation**: Review README.md, TEMPLATE_STANDARDS.md, and AGENTS.md
2. **Search Issues**: Look for similar questions in GitHub Issues
3. **Create New Issue**: Open a new issue for specific questions or problems
4. **Join Discussions**: Participate in GitHub Discussions for broader topics

---

Thank you for contributing to making `.gitignore` templates better for everyone!
