# A collection of `.gitignore` templates

This is a comprehensive collection of `.gitignore` file templates. These templates help you manage which files should not be tracked by Git in your repositories.

All templates have been recently reorganized, standardized, and optimized to ensure:

- **Enhanced Common Patterns Directory**: Shared patterns organized in `common/` with improved structure and organization
- **Reduced Duplication**: Common patterns extracted to shared files with better categorization
- **Standardized Formatting**: Consistent structure across all templates with visual separators
- **Improved Organization**: Logical categorization with clear section comments and better documentation
- **Enhanced Maintainability**: Easier to update and extend templates with comprehensive notes
- **Official Source Integration**: Templates reference official GitHub repositories for accuracy
- **Standard Template Structure**: All templates follow a consistent organizational structure
- **Code Quality Improvements**: Enhanced comments, better organization, and consistent naming
- **Recent Reorganization**: Common patterns significantly improved with better categorization and documentation

## Enhanced Organization Structure

### Core Categories
- **`languages/`** - Programming language templates (28 templates)
- **`frameworks/`** - Web and application framework templates (30 templates)
- **`tools/`** - Build, deployment, and development tool templates (37 templates)
- **`ides/`** - Code editor and IDE templates (14 templates)
- **`os/`** - Operating system file templates (3 templates)
- **`platforms/`** - Development platform templates (3 templates)

### Enhanced Common Patterns Directory
- **`common/`** - Shared patterns for better organization and reuse with improved structure:
  - `security.gitignore` - Security-sensitive files (.env*, certificates, secrets, etc.) with comprehensive security patterns
  - `build.gitignore` - Build artifacts, distribution outputs, and compiled files with better categorization
  - `dependencies.gitignore` - Dependency directories and package management organized by technology
  - `logs.gitignore` - Log files, temporary storage, and runtime data with comprehensive coverage
  - `cache.gitignore` - Cache directories and temporary files
  - `backup.gitignore` - Backup files and editor temporary files
  - `git.gitignore` - Git metadata and temporary files
  - `testing.gitignore` - Test outputs, coverage reports, and quality tools with modern testing patterns

## Standard Template Structure

All templates in this repository follow a consistent organizational structure:

### 1. Header Section
- Source attribution: `# Template from gitignores.com - Online .gitignore generator`
- Technology name and brief description
- Clear section organization with visual separators (`# ============================================================================`)

### 2. Technology-Specific Patterns
- Organized into logical categories with clear headers (`# ----------------------------------------------------------------------------`)
- Patterns sorted alphabetically within each category
- Comprehensive coverage of technology-specific artifacts
- Descriptive comments explaining pattern purposes

### 3. Common Patterns Reference
- References to relevant common patterns in the `common/` directory
- Examples of how to combine templates with common patterns
- Clear guidance on comprehensive coverage
- Best practices for template combination

### 4. Official Sources
- Links to official GitHub repositories or documentation
- Attribution for patterns based on official sources
- References to community best practices

### 5. Usage Notes
- Important usage information and considerations
- Recommendations for production projects
- Guidance on customization and best practices
- Security considerations and warnings

## Benefits of the Enhanced Organization

1. **Reduced Duplication**: Common patterns (like `.env`, `node_modules/`, `build/`) are now in shared files with better organization
2. **Better Maintenance**: Update common patterns in one place instead of multiple templates
3. **Improved Readability**: Templates focus on technology-specific patterns with clear organization and visual separators
4. **Flexible Usage**: Combine common patterns with specific templates as needed
5. **Official Source Accuracy**: Templates reference official GitHub repositories for up-to-date patterns
6. **Consistent Experience**: All templates follow the same structure for easy navigation
7. **Enhanced Documentation**: Clear guidance on usage and combination strategies with comprehensive notes
8. **Better Categorization**: Patterns organized by technology type and purpose for easier understanding
9. **Security Focus**: Clear guidance on security-critical patterns and best practices
10. **Modern Coverage**: Includes patterns for modern development tools and practices

## File Naming Conventions

All template files in this repository follow consistent URL-friendly naming conventions:

1. **Official Technology Names**: File names use the official name of the technology, converted to a URL-friendly format
2. **Lowercase**: All file names are lowercase
3. **Underscore/Hyphen Separation**: Multi-word names use underscores or hyphens as appropriate (e.g., `vscode.gitignore`, `next_js.gitignore`)
4. **Special Characters**: Special characters like `.` are removed (e.g., `Next.js` becomes `next_js.gitignore`)
5. **Consistency**: Names are consistent across all categories for easy reference

### Examples:
- **Technology**: `Next.js` → **File**: `next_js.gitignore` (not `next-js.gitignore`)
- **Technology**: `Visual Studio Code` → **File**: `vscode.gitignore` (simplified)
- **Technology**: `C#` → **File**: `c_sharp.gitignore` (added underscore for readability)
- **Technology**: `AdonisJS` → **File**: `adonis_js.gitignore` (added underscore for clarity)

This naming convention ensures:
- **Easy Discovery**: Files are easy to find and reference
- **Consistency**: Uniform naming across all templates
- **URL-Friendly**: Names work well in URLs and documentation
- **Predictability**: Users can guess file names based on technology names

For more information about how `.gitignore` files work, and how to use them, the following resources are a great place to start:

- The [Ignoring Files chapter](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#_ignoring) of the [Pro Git](https://git-scm.com/book) book.
- The [Ignoring Files article](https://help.github.com/articles/ignoring-files) on the GitHub Help site.
- The [gitignore(5)](https://git-scm.com/docs/gitignore) manual page.

It is recommended that you either [add these to your global template](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files#configuring-ignored-files-for-all-repositories-on-your-computer) or merge these rules into your project-specific templates if you want to use them permanently.

## Available templates

### Language templates (in `languages/` directory)

- `clojure.gitignore` - Clojure projects
- `cpp.gitignore` - C++ projects
- `c_sharp.gitignore` - C# projects
- `dart.gitignore` - Dart projects
- `elixir.gitignore` - Elixir projects
- `f_sharp.gitignore` - F# projects
- `go.gitignore` - Go projects
- `haskell.gitignore` - Haskell projects
- `java.gitignore` - Java projects
- `javascript.gitignore` - JavaScript projects
- `julia.gitignore` - Julia projects
- `kotlin.gitignore` - Kotlin projects
- `lua.gitignore` - Lua projects
- `node_js.gitignore` - Node.js projects
- `nim.gitignore` - Nim projects
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
- `typescript.gitignore` - TypeScript projects
- `zig.gitignore` - Zig projects

### Operating System templates (in `os/` directory)

- `linux.gitignore` - Linux system files
- `macos.gitignore` - macOS system files
- `windows.gitignore` - Windows system files

### Editor and IDE templates (in `ides/` directory)

- `android_studio.gitignore` - Android Studio IDE
- `atom.gitignore` - Atom editor
- `eclipse.gitignore` - Eclipse IDE
- `emacs.gitignore` - Emacs editor
- `fleet.gitignore` - Fleet IDE
- `intellij.gitignore` - JetBrains IDEs (IntelliJ, PyCharm, WebStorm, etc.)
- `kate.gitignore` - Kate editor
- `nano.gitignore` - Nano editor
- `netbeans.gitignore` - NetBeans IDE
- `nova.gitignore` - Nova editor
- `sublime.gitignore` - Sublime Text editor
- `vim.gitignore` - Vim editor
- `vscode.gitignore` - Visual Studio Code
- `xcode.gitignore` - Xcode IDE

### Framework templates (in `frameworks/` directory)

- `adonis_js.gitignore` - AdonisJS Node.js framework
- `angular.gitignore` - Angular framework
- `django.gitignore` - Django Python web framework
- `drupal.gitignore` - Drupal content management system
- `docusaurus.gitignore` - Docusaurus documentation framework
- `eleventy.gitignore` - Eleventy static site generator
- `ember.gitignore` - Ember.js framework
- `express.gitignore` - Express.js Node.js framework
- `fastapi.gitignore` - FastAPI Python web framework
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
- `rails.gitignore` - Ruby on Rails framework
- `prestashop.gitignore` - PrestaShop e-commerce platform
- `react.gitignore` - React framework
- `remix.gitignore` - Remix full-stack React framework
- `spring_boot.gitignore` - Spring Boot Java framework
- `svelte.gitignore` - Svelte framework
- `symfony.gitignore` - Symfony PHP framework
- `vue.gitignore` - Vue.js framework
- `wordpress.gitignore` - WordPress content management system

### Platform templates (in `platforms/` directory)

- `android.gitignore` - Android development
- `ios.gitignore` - iOS development
- `unity.gitignore` - Unity game engine

### Tool templates (in `tools/` directory)

- `ansible.gitignore` - Ansible configuration management
- `aws_codebuild.gitignore` - AWS CodeBuild CI/CD service
- `azure_devops.gitignore` - Azure DevOps CI/CD platform
- `babel.gitignore` - Babel JavaScript compiler
- `bun.gitignore` - Bun JavaScript runtime
- `circleci.gitignore` - CircleCI continuous integration
- `cmake.gitignore` - CMake build system
- `composer.gitignore` - Composer PHP dependency manager
- `cypress.gitignore` - Cypress testing framework
- `deno.gitignore` - Deno JavaScript/TypeScript runtime
- `docker.gitignore` - Docker containers and builds
- `eslint.gitignore` - ESLint & Prettier code quality tools
- `github_actions.gitignore` - GitHub Actions workflows
- `gitlab_ci.gitignore` - GitLab CI/CD pipelines
- `google_cloud_build.gitignore` - Google Cloud Build CI/CD
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
- `travis_ci.gitignore` - Travis CI continuous integration
- `turbo.gitignore` - Turborepo build system
- `vite.gitignore` - Vite build tool for modern web development
- `webpack.gitignore` - Webpack module bundler
- `yarn.gitignore` - Yarn package manager

## How to use

1. **For a specific project**: Copy the relevant template to your project's root directory and rename it to `.gitignore`:

   ```bash
   cp languages/python.gitignore .gitignore
   ```

2. **For global use**: Add templates to your global gitignore file:

   ```bash
   git config --global core.excludesfile ~/.gitignore_global
   cat os/macos.gitignore >> ~/.gitignore_global
   cat ides/intellij.gitignore >> ~/.gitignore_global
   ```

3. **Combine multiple templates**: You can combine templates for complex projects:

   ```bash
   cat languages/python.gitignore ides/intellij.gitignore > .gitignore
   ```

4. **Use common patterns**: Combine common patterns with specific templates:

   ```bash
   cat common/security.gitignore common/dependencies.gitignore languages/python.gitignore > .gitignore
   ```

5. **Create comprehensive setup**: For production projects, combine multiple common patterns:

   ```bash
   cat common/security.gitignore common/dependencies.gitignore common/build.gitignore languages/python.gitignore > .gitignore
   ```

## Contributing

We'd love for you to help us improve this project. Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute.

## License

[MIT License](LICENSE)
