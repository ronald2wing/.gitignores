# .gitignores Templates Collection

A curated collection of **129 standardized `.gitignore` templates** for programming languages, frameworks, tools, and development environments. All templates follow consistent structure and organization defined in [`TEMPLATE_STANDARDS.md`](TEMPLATE_STANDARDS.md), ensuring security-first approach and comprehensive coverage.

**Online Reference**: [gitignores.com](https://gitignores.com) – Online .gitignore generator and template reference

## 📋 Quick Navigation

- [🚀 Quick Start](#-quick-start)
- [🎯 Template Philosophy](#-template-philosophy)
- [📖 Usage Examples](#-usage-examples)
- [📁 Template Highlights](#-template-highlights)
- [🔧 Troubleshooting](#-troubleshooting)
- [🤝 Contributing](#-contributing)
- [❓ FAQ](#-faq)

## 🚀 Quick Start

### Choose Your Approach

| Use Case                         | Recommended Approach         | Example                                                    |
| -------------------------------- | ---------------------------- | ---------------------------------------------------------- |
| **Framework/Full-stack project** | Single framework template    | `frameworks/react.gitignore`                               |
| **Language-only project**        | Language + security template | `languages/python.gitignore` + `common/security.gitignore` |
| **Custom toolchain**             | Combine multiple templates   | Language + common + tools + IDE                            |

### Download & Test

```bash
# Download a template
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/react.gitignore

# Test it works
git init
touch .env node_modules/test.js dist/bundle.js
git status --ignored
```

## 🎯 Template Philosophy

### Two Complementary Approaches

#### 1. **Framework Templates** (`frameworks/`)

**Simple, complete, security-first** – For most users
- ✅ Self-contained: security + framework + language patterns
- ✅ Security patterns placed FIRST
- ✅ Everything needed in one file
- ❌ Don't combine with language templates (duplicates)

**Example**: `frameworks/react.gitignore` includes security, React, JavaScript, and common patterns.

#### 2. **Language + Common Templates** (`languages/` + `common/`)

**Modular, customizable** – For advanced users
- ✅ Language-specific patterns only
- ✅ Combine with common templates as needed
- ✅ Granular control over what's included
- ⚠️ Always include `common/security.gitignore`

**Example**: Custom Python setup with security, cache, and Docker patterns.

### ⚠️ Critical Rule

**Never combine framework templates with language templates** – Framework templates already include all necessary language patterns.

## 📖 Usage Examples

### Basic Examples

```bash
# React project (framework template)
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/react.gitignore

# Python web project (language + common)
cat languages/python.gitignore \
    common/security.gitignore \
    common/cache.gitignore \
    tools/docker.gitignore > .gitignore

# Multi-platform project
cat frameworks/react.gitignore \
    os/linux.gitignore \
    os/macos.gitignore \
    os/windows.gitignore > .gitignore
```

### Advanced Techniques

```bash
# Remove duplicates when combining
cat template1 template2 template3 | sort -u > .gitignore

# Test specific patterns
git check-ignore -v .env.local
git check-ignore -v node_modules/package.json

# Check all ignored files
git status --ignored
```

### Real-World Scenarios

```bash
# Full-stack JavaScript: React + Docker + VS Code
cat frameworks/react.gitignore \
    tools/docker.gitignore \
    ides/visual-studio-code.gitignore > .gitignore

# Data Science: Python + Jupyter + Docker
cat languages/python.gitignore \
    common/security.gitignore \
    tools/jupyter.gitignore \
    tools/docker.gitignore > .gitignore
```

## 📁 Template Highlights

### 📊 Overview

| Category       | Count | Key Examples                           |
| -------------- | ----- | -------------------------------------- |
| **Common**     | 7     | `security.gitignore` (CRITICAL)        |
| **Frameworks** | 34    | `django.gitignore`, `react.gitignore`  |
| **Languages**  | 31    | `python.gitignore`, `node.gitignore`   |
| **Tools**      | 37    | `docker.gitignore`, `npm.gitignore`    |
| **IDEs**       | 14    | `visual-studio-code.gitignore`         |
| **OS**         | 3     | `macos.gitignore`, `windows.gitignore` |
| **Platforms**  | 3     | `android.gitignore`, `ios.gitignore`   |
| **Total**      | **129** |                                       |

### 🔐 Common Templates (Essential)

- `security.gitignore` – **CRITICAL**: `.env*`, credentials, sensitive files
- `build.gitignore` – Build artifacts and temporary files
- `cache.gitignore` – Cache directories and temporary files
- `logs.gitignore` – Log files and runtime artifacts
- `backup.gitignore` – Backup files and temporary copies
- `git.gitignore` – Git-specific files and metadata
- `testing.gitignore` – Testing artifacts and coverage reports

### 🏗️ Popular Framework Templates

- **Web**: `django.gitignore`, `ruby-on-rails.gitignore`, `laravel.gitignore`, `spring-boot.gitignore`
- **JavaScript**: `react.gitignore`, `vue.gitignore`, `angular.gitignore`, `nextjs.gitignore`
- **Mobile**: `flutter.gitignore`, `react-native.gitignore`, `ionic.gitignore`
- **CMS**: `wordpress.gitignore`, `drupal.gitignore`, `joomla.gitignore`

### 💻 Popular Language Templates

- **Popular**: `python.gitignore`, `javascript.gitignore`, `java.gitignore`, `csharp.gitignore`
- **Web**: `typescript.gitignore`, `php.gitignore`, `html.gitignore`, `css.gitignore`
- **Systems**: `rust.gitignore`, `go.gitignore`, `cpp.gitignore`, `c.gitignore`
- **Scripting**: `bash.gitignore`, `powershell.gitignore`, `perl.gitignore`

### 🛠️ Essential Tool Templates

- **Package Managers**: `npm.gitignore`, `yarn.gitignore`, `composer.gitignore`, `pip.gitignore`
- **Build Tools**: `webpack.gitignore`, `vite.gitignore`, `docker.gitignore`
- **Testing**: `jest.gitignore`, `pytest.gitignore`, `cypress.gitignore`
- **CI/CD**: `github-actions.gitignore`, `gitlab-ci.gitignore`

### 💾 Popular IDE Templates

- `visual-studio-code.gitignore`
- `intellij.gitignore`
- `vim.gitignore`
- `emacs.gitignore`

## 🔧 Troubleshooting

For comprehensive troubleshooting guidance, debugging workflows, and solutions to common issues, refer to the [Troubleshooting section in AGENTS.md](AGENTS.md#-troubleshooting). This includes detailed solutions for:

- Files not being ignored
- Performance problems with large `.gitignore` files
- Template combination conflicts
- Security patterns missing
- Debugging workflow and testing procedures

## 🤝 Contributing

We welcome contributions! Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for detailed guidelines.

### Quick Contribution Guide

1. **Fork** the repository
2. **Create a branch** for your changes
3. **Follow** [`TEMPLATE_STANDARDS.md`](TEMPLATE_STANDARDS.md) exactly
4. **Test** your template thoroughly
5. **Submit** a pull request with clear description

### Types of Contributions

- **New Templates**: Create templates for new technologies
- **Template Improvements**: Update existing templates
- **Bug Fixes**: Correct errors in existing templates
- **Documentation**: Improve documentation

## ❓ FAQ

### Q: Should I use framework or language templates?
**A**: Use framework templates for complete projects (React, Django, etc.). Use language + common templates for custom setups or when you need granular control.

### Q: Why are security patterns separate in language templates?
**A**: Language templates focus on language-specific patterns. Security patterns are in `common/security.gitignore` to ensure they're always included when needed and to avoid duplication.

### Q: How do I combine multiple templates?
**A**: Use `cat` to combine templates, then `sort -u` to remove duplicates:
```bash
cat template1 template2 template3 | sort -u > .gitignore
```

### Q: What if my template isn't working?
**A**:
1. Check file location: `.gitignore` should be in repository root
2. Test patterns: `git check-ignore -v <file>`
3. Check for conflicts: `git status --ignored`
4. Verify no syntax errors in patterns

### Q: Can I suggest a new template?
**A**: Yes! Open an issue or submit a pull request. Check if the template already exists first.

### Q: How often are templates updated?
**A**: Templates are reviewed quarterly for accuracy and updated when technologies release new versions.

---

**Maintained by**: [gitignores.com](https://gitignores.com)
**Repository**: <https://github.com/ronald2wing/.gitignores>
**Online Tool**: <https://gitignores.com>
