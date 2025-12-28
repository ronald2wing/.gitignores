# .gitignores Templates Collection

A comprehensive collection of `.gitignore` templates for programming languages, frameworks, tools, and development environments. These templates help you manage which files should not be tracked by Git in your repositories.

## Quick Start

### Download a Template
```bash
# Python project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/languages/python.gitignore

# React project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/react.gitignore

# Django project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/django.gitignore
```

### Or Clone the Repository
```bash
git clone https://github.com/ronald2wing/.gitignores.git
```

## Table of Contents

- [Quick Start](#quick-start)
- [Installation](#installation)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Design Philosophy](#design-philosophy)
- [Best Practices](#best-practices)
- [Available Templates](#available-templates)
- [Contributing](#contributing)
- [License](#license)

## Installation

### Quick Download

Download templates directly using curl:

```bash
# For a Python project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/languages/python.gitignore

# For a React project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/react.gitignore

# For a Django project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/django.gitignore

# For a Node.js project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/languages/node_js.gitignore
```

### Alternative Methods

You can also clone the repository or use it as a submodule:

```bash
# Clone the repository
git clone https://github.com/ronald2wing/.gitignores.git

# Or use as a submodule
git submodule add https://github.com/ronald2wing/.gitignores.git
```

## Usage

### Quick Start

#### Download Templates

```bash
# Node.js project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/languages/node_js.gitignore

# Python project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/languages/python.gitignore

# React project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/react.gitignore

# Spring Boot project
curl -o .gitignore https://raw.githubusercontent.com/ronald2wing/.gitignores/master/frameworks/spring-boot.gitignore
```

#### Clone Repository

```bash
git clone https://github.com/ronald2wing/.gitignores.git
```

### Usage Approaches

#### Option 1: Comprehensive Framework Templates (Recommended)

Framework templates are self-contained with all necessary patterns for that framework, including:

- Framework-specific patterns
- Relevant ecosystem patterns (e.g., Node.js patterns for React)
- Security patterns (`.env*` files)
- Dependency directories
- Build artifacts and cache files

```bash
# Simple approach - just use the framework template
cp frameworks/react.gitignore .gitignore
```

#### Option 2: Modular Template Combination (Advanced)

Combine language and category templates for granular control:

```bash
# Modular approach for custom Node.js project
cat languages/node_js.gitignore \
    common/security.gitignore \
    common/cache.gitignore \
    common/logs.gitignore \
    common/backup.gitignore \
    ides/visual-studio-code.gitignore \
    os/linux.gitignore \
    os/macos.gitignore \
    os/windows.gitignore > .gitignore
```

**Important**: Do not combine framework templates with language templates - framework templates already include relevant language patterns.

### Usage Examples

```bash
# React Project (Simple Comprehensive Approach)
cp frameworks/react.gitignore .gitignore

# Custom Node.js Project (Modular Approach)
cat languages/node_js.gitignore \
    common/security.gitignore \
    common/cache.gitignore \
    common/logs.gitignore \
    common/backup.gitignore \
    ides/visual-studio-code.gitignore \
    os/linux.gitignore \
    os/macos.gitignore \
    os/windows.gitignore > .gitignore

# Django Project (Simple Comprehensive Approach)
cp frameworks/django.gitignore .gitignore

# Java + Spring Boot + Maven Project (Enterprise)
cat languages/java.gitignore \
    frameworks/spring-boot.gitignore \
    common/security.gitignore \
    common/cache.gitignore \
    common/logs.gitignore \
    common/backup.gitignore \
    os/linux.gitignore \
    os/macos.gitignore \
    os/windows.gitignore \
    ides/intellij.gitignore > .gitignore

# Minimal Node.js Project (Essential Only)
cat languages/node_js.gitignore \
    common/security.gitignore \
    common/cache.gitignore > .gitignore
```

**Tip**: Use `sort -u` to remove duplicate patterns: `cat template1 template2 | sort -u > .gitignore`

## Folder Structure

The repository is organized into logical categories for maintainability:

```
.
├── common/          # Shared patterns (7 templates)
├── languages/       # Programming languages (28 templates)
├── frameworks/      # Web/application frameworks (31 templates)
├── tools/          # Build/deployment tools (37 templates)
├── ides/           # Code editors/IDEs (14 templates)
├── os/             # Operating systems (3 templates)
└── platforms/      # Development platforms (3 templates)
```

### Common Patterns (`common/`)

Shared patterns applicable across multiple technologies:

- `security.gitignore` - Security-sensitive files (.env*, certificates, secrets)
- `build.gitignore` - Build artifacts and compiled files
- `logs.gitignore` - Log files and runtime data
- `cache.gitignore` - Cache directories and temporary files
- `backup.gitignore` - Backup files and editor temporaries
- `git.gitignore` - Git metadata and temporary files
- `testing.gitignore` - Test outputs and coverage reports

## Design Philosophy

### Language Templates (Reference Model)
- Contain **only** language-specific patterns
- Reference common patterns from `common/` directory
- Users combine templates as needed: `cat common/security.gitignore common/build.gitignore languages/language.gitignore > .gitignore`

### Framework Templates (Standalone Model)
- Comprehensive and self-contained
- Include framework-specific patterns, language patterns, and essential common patterns
- Users can use single framework templates without combining multiple files

### Reference Template (Source of Truth)
- **`reference_template.gitignore`** serves as the definitive reference for all template types
- Demonstrates proper structure, formatting, and organization for each template category
- Follows security-first approach with organized sections and alphabetical pattern sorting
- All templates in this repository follow the standards established in the reference template

### Benefits
- **Simplified Usage**: Single templates for frameworks, flexible combinations for languages
- **Better Organization**: Clear separation of concerns
- **Improved Maintenance**: Updates localized to specific templates
- **Reduced Duplication**: Common patterns in shared files
- **Consistent Standards**: All templates follow the reference template structure

## Template Structure

All templates in this repository follow the structure, formatting, and organization standards established in the reference template `reference_template.gitignore`. This template serves as the definitive source of truth for all template types.

For detailed template structure guidelines, key principles, and practical creation examples, refer to [CONTRIBUTING.md](CONTRIBUTING.md#template-structure).

## Best Practices

### 1. Customize for Your Project

Add project-specific exclusions for:
- Build artifacts and temporary files
- Database dumps and backups
- Large media files
- Sensitive files (API keys, certificates, credentials)

### 2. Test and Validate

Ensure your `.gitignore` file works correctly:
- Run `git status` to see what files are being tracked
- Verify essential files are not accidentally excluded
- Check that ignored files don't appear in `git status` output

### 3. Maintain and Update

Keep your `.gitignore` file current:
- Review periodically as your project evolves
- Add patterns for new tools and dependencies
- Remove patterns for tools no longer used
- Document patterns with comments for future maintainers

### 4. Pattern Ordering

Place more specific patterns before general ones. Git processes patterns in order, and the first matching pattern wins.

### 5. Use Template Combinations Effectively

- **Framework Templates**: Use single framework templates for simplicity and completeness
- **Language + Common Templates**: Combine for granular control when needed
- **Avoid Duplication**: Don't combine framework templates with language templates (they already include language patterns)
- **Remove Duplicates**: Use `sort -u` when combining multiple templates

### 6. Security Considerations

- Always include security patterns (`.env*`, certificates, secrets)
- Review patterns to ensure sensitive files are excluded
- Consider using separate `.gitignore` files for different environments
- Document security-sensitive patterns clearly

### 7. Performance Optimization

- Exclude large directories (node_modules/, vendor/, etc.)
- Ignore cache and temporary files
- Consider excluding generated files that can be rebuilt
- Use wildcards carefully to avoid unintended exclusions

### 8. Team Collaboration

- Keep `.gitignore` files in version control
- Document non-obvious patterns with comments
- Review `.gitignore` changes during code reviews
- Ensure all team members understand the patterns

## Available Templates

### Language templates (in `languages/` directory)

- `c_sharp.gitignore` - C# projects
- `clojure.gitignore` - Clojure projects
- `cpp.gitignore` - C++ projects
- `dart.gitignore` - Dart projects
- `elixir.gitignore` - Elixir projects
- `f_sharp.gitignore` - F# projects
- `go.gitignore` - Go projects
- `haskell.gitignore` - Haskell projects
- `java.gitignore` - Java projects
- `java_script.gitignore` - JavaScript projects
- `julia.gitignore` - Julia projects
- `kotlin.gitignore` - Kotlin projects
- `lua.gitignore` - Lua projects
- `nim.gitignore` - Nim projects
- `node_js.gitignore` - Node.js projects
- `ocaml.gitignore` - OCaml projects
- `perl.gitignore` - Perl projects
- `php.gitignore` - PHP projects
- `powershell.gitignore` - PowerShell projects
- `python.gitignore` - Python projects
- `r.gitignore` - R projects
- `ruby.gitignore` - Ruby projects
- `rust.gitignore` - Rust projects
- `scala.gitignore` - Scala projects
- `shell.gitignore` - Shell/Bash scripting
- `swift.gitignore` - Swift projects
- `type_script.gitignore` - TypeScript projects
- `zig.gitignore` - Zig projects

### Operating System templates (in `os/` directory)

- `linux.gitignore` - Linux system files
- `macos.gitignore` - macOS system files
- `windows.gitignore` - Windows system files

### Editor and IDE templates (in `ides/` directory)

- `android-studio.gitignore` - Android Studio IDE
- `atom.gitignore` - Atom editor
- `eclipse.gitignore` - Eclipse IDE
- `emacs.gitignore` - Emacs editor
- `fleet.gitignore` - Fleet IDE
- `intellij.gitignore` - JetBrains IDEs (IntelliJ, PyCharm, WebStorm, etc.)
- `kate.gitignore` - Kate editor
- `nano.gitignore` - Nano editor
- `netbeans.gitignore` - NetBeans IDE
- `nova.gitignore` - Nova editor
- `sublime-text.gitignore` - Sublime Text editor
- `vim.gitignore` - Vim editor
- `visual-studio-code.gitignore` - Visual Studio Code
- `xcode.gitignore` - Xcode IDE

### Framework templates (in `frameworks/` directory)

- `adonis_js.gitignore` - AdonisJS Node.js framework
- `angular.gitignore` - Angular framework
- `django.gitignore` - Django Python web framework
- `docusaurus.gitignore` - Docusaurus documentation framework
- `dot_net.gitignore` - .NET framework
- `drupal.gitignore` - Drupal content management system
- `eleventy.gitignore` - Eleventy static site generator
- `ember.gitignore` - Ember.js framework
- `express_js.gitignore` - Express.js Node.js framework
- `fast_api.gitignore` - FastAPI Python web framework
- `flask.gitignore` - Flask Python web framework
- `flutter.gitignore` - Flutter mobile framework
- `gatsby.gitignore` - Gatsby static site generator
- `hugo.gitignore` - Hugo static site generator
- `jekyll.gitignore` - Jekyll static site generator
- `joomla.gitignore` - Joomla content management system
- `laravel.gitignore` - Laravel PHP framework
- `magento.gitignore` - Magento e-commerce platform
- `nest_js.gitignore` - NestJS Node.js framework
- `next_js.gitignore` - Next.js React framework
- `nuxt_js.gitignore` - Nuxt.js Vue.js framework
- `phoenix.gitignore` - Phoenix Elixir web framework
- `prestashop.gitignore` - PrestaShop e-commerce platform
- `react.gitignore` - React framework
- `remix.gitignore` - Remix full-stack React framework
- `ruby-on-rails.gitignore` - Ruby on Rails framework
- `spring-boot.gitignore` - Spring Boot Java framework
- `svelte.gitignore` - Svelte framework
- `symfony.gitignore` - Symfony PHP framework
- `vue_js.gitignore` - Vue.js framework
- `word_press.gitignore` - WordPress content management system

### Platform templates (in `platforms/` directory)

- `android.gitignore` - Android development
- `ios.gitignore` - iOS development
- `unity.gitignore` - Unity game engine

### Tool templates (in `tools/` directory)

- `ansible.gitignore` - Ansible configuration management
- `aws-codebuild.gitignore` - AWS CodeBuild CI/CD service
- `azure-devops.gitignore` - Azure DevOps CI/CD platform
- `babel.gitignore` - Babel JavaScript compiler
- `bun.gitignore` - Bun JavaScript runtime
- `circleci.gitignore` - CircleCI continuous integration
- `cmake.gitignore` - CMake build system
- `composer.gitignore` - Composer PHP dependency manager
- `cypress.gitignore` - Cypress testing framework
- `deno.gitignore` - Deno JavaScript/TypeScript runtime
- `docker.gitignore` - Docker containers and builds
- `eslint.gitignore` - ESLint & Prettier code quality tools
- `github-actions.gitignore` - GitHub Actions workflows
- `gitlab-ci.gitignore` - GitLab CI/CD pipelines
- `google-cloud-build.gitignore` - Google Cloud Build CI/CD
- `gradle.gitignore` - Gradle build tool for Java/Kotlin
- `grunt.gitignore` - Grunt task runner
- `gulp.gitignore` - Gulp task runner
- `jenkins.gitignore` - Jenkins CI/CD tool
- `jest.gitignore` - Jest testing framework
- `jupyter.gitignore` - Jupyter Notebook
- `kubernetes.gitignore` - Kubernetes container orchestration
- `make.gitignore` - Make build tool
- `maven.gitignore` - Maven build tool for Java
- `mocha.gitignore` - Mocha testing framework
- `npm.gitignore` - npm / yarn package manager
- `parcel.gitignore` - Parcel web application bundler
- `pipenv.gitignore` - Pipenv Python dependency manager
- `poetry.gitignore` - Poetry Python dependency manager
- `rollup.gitignore` - Rollup module bundler
- `sphinx.gitignore` - Sphinx documentation generator
- `terraform.gitignore` - Terraform infrastructure as code
- `travis-ci.gitignore` - Travis CI continuous integration
- `turbo.gitignore` - Turborepo build system
- `vite.gitignore` - Vite build tool for modern web development
- `webpack.gitignore` - Webpack module bundler
- `yarn.gitignore` - Yarn package manager

## Contributing

We'd love for you to help us improve this project. Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute.

## License

[MIT License](LICENSE)
