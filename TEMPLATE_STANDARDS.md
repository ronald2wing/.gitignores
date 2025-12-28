# Gitignores Template Standards

**Repository**: [ronald2wing/.gitignores](https://github.com/ronald2wing/.gitignores)
**Online Reference**: [gitignores.com](https://gitignores.com)
**Purpose**: Definitive standards for all `.gitignore` templates in this repository
**Usage**: Reference for template creation and maintenance
**Required**: All templates must follow these standards exactly

## 📋 Table of Contents

1. [📝 Template Header Format](#1-template-header-format-required)
2. [📋 Template Metadata & Usage](#2-template-metadata--usage-required)
3. [📁 Template Categories & Structure](#3-template-categories--structure)
4. [🔧 Pattern Organization & Formatting](#4-pattern-organization--formatting)
5. [🔐 Security Patterns & Best Practices](#5-security-patterns--best-practices-critical)
6. [📝 File Naming Conventions](#6-file-naming-conventions)
7. [✅ Template Validation Checklist](#7-template-validation-checklist)
8. [🔄 Template Usage & Combination](#8-template-usage--combination)
9. [🧪 Template Testing & Validation](#9-template-testing--validation)
10. [🔄 Maintenance & Quality Assurance](#10-maintenance--quality-assurance)

---

## 1. Template Header Format (REQUIRED)

Every template MUST begin with this exact header format:

```gitignore
# ============================================================================
# Created by https://gitignores.com/
# [TEMPLATE TYPE] for [Technology Name]
# Website: [Official website URL]
# Repository: [Official GitHub repository URL or https://github.com/ronald2wing/.gitignores]
# ============================================================================
```

### Template Types (use exactly as shown)

- **LANGUAGE-SPECIFIC TEMPLATE** for [Language]
- **COMPREHENSIVE FRAMEWORK TEMPLATE** for [Framework]
- **TOOL-SPECIFIC TEMPLATE** for [Tool]
- **IDE/EDITOR TEMPLATE** for [IDE]
- **OPERATING SYSTEM TEMPLATE** for [OS]
- **PLATFORM-SPECIFIC TEMPLATE** for [Platform]
- **COMMON PATTERNS TEMPLATE** for [Category]

### Header Examples

```gitignore
# ============================================================================
# Created by https://gitignores.com/
# COMPREHENSIVE FRAMEWORK TEMPLATE for Django
# Website: https://www.djangoproject.com/
# Repository: https://github.com/django/django
# ============================================================================
```

```gitignore
# ============================================================================
# Created by https://gitignores.com/
# LANGUAGE-SPECIFIC TEMPLATE for Python
# Website: https://www.python.org/
# Repository: https://github.com/python/cpython
# ============================================================================
```

---

## 2. Template Metadata & Usage (REQUIRED)

Every template MUST include this metadata section immediately after the header:

```gitignore
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# TEMPLATE OVERVIEW & USAGE NOTES
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# • TEMPLATE TYPE: [Type from above]
# • PURPOSE: [Brief description of template purpose]
# • DESIGN PHILOSOPHY: [Self-contained vs modular approach]
# • COMBINATION GUIDANCE: [How to combine with other templates]
# • SECURITY CONSIDERATIONS: [Security patterns included or needed]
# • BEST PRACTICES: [Key recommendations for usage]
# • OFFICIAL SOURCES: [Technology] community patterns and best practices
```

### Complete Metadata Example

```gitignore
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# TEMPLATE OVERVIEW & USAGE NOTES
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# • TEMPLATE TYPE: COMPREHENSIVE FRAMEWORK TEMPLATE
# • PURPOSE: Django web framework specific ignore patterns
# • DESIGN PHILOSOPHY: Self-contained with all Django-specific patterns
# • COMBINATION GUIDANCE: Use standalone, do NOT combine with python.gitignore
# • SECURITY CONSIDERATIONS: Includes security patterns for .env files and credentials
# • BEST PRACTICES: Review before use, test with your specific Django setup
# • OFFICIAL SOURCES: Django community patterns and best practices
```

---

## 3. Template Categories & Structure

### Framework Templates (`frameworks/` directory)

- **Self-contained** with ALL necessary patterns
- **Security patterns FIRST** (critical for protection)
- Include framework-specific + language + essential common patterns
- **Examples**: `frameworks/django.gitignore`, `frameworks/react.gitignore`
- **DO NOT combine** with language templates (duplicates)

### Language Templates (`languages/` directory)

- **Language-specific patterns ONLY**
- **NO security patterns** (use `common/security.gitignore`)
- Designed for combination with common templates
- **Examples**: `languages/python.gitignore`, `languages/node.gitignore`
- **Combine with** common templates for complete coverage

### Common Templates (`common/` directory)

- **Shared patterns** across technologies
- Security, build, cache, logs, backup, git, testing
- Use with language templates for comprehensive coverage
- **Examples**: `common/security.gitignore`, `common/cache.gitignore`
- **Essential**: Always include `common/security.gitignore` with language templates

### Tool Templates (`tools/` directory)

- **Tool-specific patterns** only
- Build tools, package managers, CI/CD tools
- Combine with language templates as needed
- **Examples**: `tools/docker.gitignore`, `tools/npm.gitignore`
- **Optional**: Add based on project tooling

### IDE Templates (`ides/` directory)

- **Editor/IDE configuration** and cache files
- Combine with language or framework templates
- **Examples**: `ides/visual-studio-code.gitignore`, `ides/intellij.gitignore`
- **Optional**: Add based on team IDE preferences

### OS Templates (`os/` directory)

- **Operating system-specific** files
- Combine with other templates as needed
- **Examples**: `os/linux.gitignore`, `os/macos.gitignore`, `os/windows.gitignore`
- **Recommended**: Include all OS templates for cross-platform projects

### Platform Templates (`platforms/` directory)

- **Development platform-specific** patterns
- Combine with language templates as needed
- **Examples**: `platforms/android.gitignore`, `platforms/ios.gitignore`
- **Required** for platform-specific development

---

## 4. Pattern Organization & Formatting

### Section Header Format

```gitignore
# ••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••
# SECTION TITLE
# ••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••
# [Optional brief description]
```

### Section Order (when applicable)

1. **Security & Sensitive Data Protection** (framework templates ONLY)
2. **Build Artifacts & Distribution**
3. **Dependency Management & Package Cache**
4. **Development & Runtime Artifacts**
5. **Testing & Quality Assurance**
6. **Documentation & Examples**
7. **Tool-Specific Patterns**
8. **IDE/Editor Specific Files**

### Pattern Organization Rules

- **Sort patterns alphabetically** within each section (case-insensitive)
- **Each pattern on its own line**
- **Use descriptive comments** for non-obvious patterns
- **NO duplicate patterns** within template
- **Use consistent indentation** (no tabs, 2 spaces if needed)

---

## 5. Security Patterns & Best Practices (CRITICAL)

Framework templates MUST include security section FIRST:

```gitignore
# ••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••
# SECURITY & SENSITIVE DATA PROTECTION (ALWAYS FIRST!)
# ••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••••
# CRITICAL: Protect sensitive data from accidental commits to version control
# WARNING: These patterns should always be included in production projects

# Essential security patterns (include in framework templates):
.env
.env.*
.env.local
.env.development.local
.env.test.local
.env.production.local
npm-debug.log*
yarn-debug.log*
yarn-error.log*
.pnpm-debug.log*
lerna-debug.log*

# Additional security patterns (as needed):
*.pem
*.key
*.crt
*.csr
*.p12
*.pfx
*.p7b
secrets.yml
credentials.json
firebase.json
service-account-key.json
```

### Security Best Practices

1. **Always include** `.env*` patterns in framework templates
2. **Place security section FIRST** for maximum visibility
3. **Use specific patterns** rather than broad wildcards
4. **Document security considerations** in template metadata
5. **Test security patterns** with sample sensitive files

---

## 6. File Naming Conventions

### File Naming Rules

- **Lowercase only**
- **URL-friendly** (no spaces, special characters)
- **Based on official technology name**

### Separator Rules

- **Hyphen (-)** for spaces: "React Native" → `react-native.gitignore`
- **Remove dots/special chars**: "Next.js" → `nextjs.gitignore`
- **No separator** for single words: "React" → `react.gitignore`

### JavaScript File Naming Rule

- **Use GitHub repository name** as the primary reference for JavaScript-related technologies
- **Remove organization prefix** from repository names (e.g., `facebook/react` → `react`)
- **Remove dots/special characters** from repository names (e.g., `vercel/next.js` → `nextjs`)
- **Use repository name as-is** without adding `.js` suffix
- **General Rule**: When GitHub repository name is not related to official technology name,
  use parent organization name
- **Example**: For AdonisJS, use `adonisjs.gitignore` (GitHub: `adonisjs/core` -
  repository name "core" unrelated to official name)
- **Examples**:
  - **React** (GitHub: `facebook/react`) → `react.gitignore` (repository name: react)
  - **Express.js** (GitHub: `expressjs/express`) → `express.gitignore` (repository name: express)
  - **Next.js** (GitHub: `vercel/next.js`) → `nextjs.gitignore` (repository name: next.js → remove dot)
  - **Vue.js** (GitHub: `vuejs/vue`) → `vue.gitignore` (repository name: vue)
  - **Angular** (GitHub: `angular/angular`) → `angular.gitignore` (repository name: angular)
  - **Node.js** (GitHub: `nodejs/node`) → `node.gitignore` (repository name: node)
  - **AdonisJS** (GitHub: `adonisjs/core`) → `adonisjs.gitignore`
    (example of general rule: repository name "core" unrelated to official name)

### Examples

| Technology Name    | Template File Name             | Rule Applied                           |
| ------------------ | ------------------------------ | -------------------------------------- |
| Visual Studio Code | `visual-studio-code.gitignore` | Hyphen for spaces                      |
| Node.js            | `node.gitignore`               | GitHub repo name: node                 |
| C#                 | `csharp.gitignore`             | Official name conversion               |
| .NET               | `dotnet.gitignore`             | Remove dot                             |
| Spring Boot        | `spring-boot.gitignore`        | Hyphen for spaces                      |
| Ruby on Rails      | `ruby-on-rails.gitignore`      | Hyphen for spaces                      |
| JavaScript         | `javascript.gitignore`         | Full language name                     |
| TypeScript         | `typescript.gitignore`         | Full language name                     |
| WordPress          | `wordpress.gitignore`          | Single word                            |
| Express.js         | `express.gitignore`            | GitHub repo name: express              |
| Next.js            | `nextjs.gitignore`             | GitHub repo name: next.js → remove dot |
| Vue.js             | `vue.gitignore`                | GitHub repo name: vue                  |
| React              | `react.gitignore`              | GitHub repo name: react                |

---

## 7. Template Validation Checklist

### ✅ File Structure

- [ ] Correct file name following naming conventions
- [ ] Template in correct directory
- [ ] Standard header format with gitignores.com attribution
- [ ] Clear usage notes and combination guidance

### ✅ Pattern Quality

- [ ] Patterns sorted alphabetically within sections
- [ ] Logical category organization with clear headers
- [ ] No duplicate patterns within template
- [ ] Security patterns included (framework templates)
- [ ] Appropriate pattern selection (not too broad, not too specific)

### ✅ Technical Accuracy

- [ ] Correct Git ignore syntax
- [ ] No syntax errors or malformed patterns
- [ ] Patterns tested with Git commands
- [ ] Essential files not accidentally excluded

### ✅ Documentation

- [ ] Clear comments for non-obvious patterns
- [ ] References to official sources
- [ ] Combination guidance with other templates
- [ ] Warnings about pattern conflicts or duplication

---

## 8. Template Usage & Combination

### 1. Framework Templates: Use standalone

```bash
# Single framework template
cp frameworks/django.gitignore .gitignore
```

### 2. Language + Common Templates: Combine for granular control

```bash
# Combine language with common templates
cat languages/python.gitignore \
    common/security.gitignore \
    common/cache.gitignore > .gitignore
```

### 3. Remove duplicates when combining

```bash
# Remove duplicate patterns
cat template1 template2 | sort -u > .gitignore
```

### 4. Test combinations

```bash
# Check what files are being ignored
git status --ignored

# Test specific file patterns
git check-ignore -v <file>
```

### 5. Practical Examples

**Example 1: Python web project**

```bash
cat languages/python.gitignore \
    common/security.gitignore \
    common/cache.gitignore \
    common/logs.gitignore \
    tools/docker.gitignore > .gitignore
```

**Example 2: JavaScript project with specific tools**

```bash
cat languages/javascript.gitignore \
    common/security.gitignore \
    tools/npm.gitignore \
    tools/webpack.gitignore \
    ides/visual-studio-code.gitignore > .gitignore
```

**Example 3: Multi-platform project**

```bash
cat frameworks/react.gitignore \
    os/linux.gitignore \
    os/macos.gitignore \
    os/windows.gitignore > .gitignore
```

---

## 9. Template Testing & Validation

### Basic Testing Commands

```bash
# Create test directory
mkdir test-project && cd test-project

# Copy template
cp ../path/to/template.gitignore .gitignore

# Initialize git
git init

# Create test files
touch .env config.json build/ dist/ node_modules/

# Check ignored files
git status --ignored

# Test specific patterns
git check-ignore -v .env.local
git check-ignore -v node_modules/package.json
```


### Testing Best Practices

1. **Test with real projects** - Use the template in actual development environments
2. **Test edge cases** - Check unusual file names and directory structures
3. **Test combinations** - Verify template works correctly with other templates
4. **Test false positives** - Ensure essential files aren't accidentally excluded
5. **Test performance** - Verify large templates don't impact Git performance

---

## 10. Maintenance & Quality Assurance

### Regular Maintenance Tasks

1. **Quarterly Review** - Review all templates every 3 months for outdated patterns
2. **Technology Updates** - Update templates when new versions of technologies are released
3. **Pattern Optimization** - Continuously optimize patterns for better performance and accuracy
4. **Documentation Updates** - Keep documentation current with template changes

### Quality Assurance Process

1. **Template Creation** - Follow all standards in this document
2. **Peer Review** - Have another maintainer review new or updated templates
3. **Testing** - Test templates with sample projects and Git commands
4. **Validation** - Run validation scripts to check for compliance
5. **Documentation** - Update documentation to reflect changes

### Community Contributions

1. **Issue Tracking** - Use GitHub Issues to track template problems and suggestions
2. **Pull Request Review** - Review community contributions for quality and security
3. **Feedback Integration** - Incorporate community feedback into template improvements
4. **Documentation Updates** - Update documentation based on community questions and issues

### Performance Considerations

1. **Large Templates** - Very large templates may impact Git performance; consider splitting if necessary
2. **Pattern Efficiency** - Use efficient patterns to minimize performance impact
3. **Testing** - Test templates with large repositories to identify performance issues

---

## Summary

These standards ensure consistency, quality, and security across all 129 templates in the repository. All contributors must follow these guidelines when creating or updating templates.

**Maintained by**: [gitignores.com](https://gitignores.com)
**Repository**: <https://github.com/ronald2wing/.gitignores>
**Online Tool**: <https://gitignores.com>
