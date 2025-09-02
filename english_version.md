[简体中文](./README.md) | **English**
# Code Stats - Ultimate Code Statistics Tool

A powerful command-line code statistics tool for in-depth analysis of codebases, providing detailed line counts, language breakdowns, and project health insights. It intelligently recognizes multiple programming languages and generates clear, formatted reports.

## ✨ Features

*   **📊 Comprehensive Language Support**: Automatically recognizes **20+** programming and markup languages including **Go, Python, JavaScript/TypeScript, Java, C/C++, Ruby, Rust, PHP, Shell**, and more.
*   **🔍 Smart File Filtering**: Automatically ignores version control directories (e.g., `.git`), dependencies (e.g., `node_modules`, `vendor`), build outputs, log files, and binaries to focus on source code.
*   **📈 Real-time Progress Display**: Provides a visual progress bar when analyzing large codebases for clear feedback (auto-disabled in debug mode).
*   **🐛 Verbose Debug Mode**: Enabled with the `-d` flag, shows the processing details and counts for each file, ideal for debugging and verification.
*   **📋 Multi-dimensional Report**:
    *   Detailed statistics grouped by programming language (Files, Total, Blank, Comment, Code lines).
    *   Project summary with **Code Density**, **Comment Ratio**, and **Average File Size**.
*   **🎨 Terminal-Friendly Output**: Uses colors to highlight key information for easy reading. Auto-disables colors when output is redirected to a file.
*   **⚙️ Flexible Target Specification**: Supports analyzing either a single file or an entire directory.

## 🚀 Installation & Usage

### Direct Usage
1.  Save the script as `code_stats.sh`.
2.  Make it executable:
    ```bash
    chmod +x code_stats.sh
    ```
3.  Run the script with your target.

### Usage
```bash
# Show help message
./code_stats.sh -h

# Analyze the current directory
./code_stats.sh .

# Analyze a specific directory
./code_stats.sh /path/to/your/project

# Analyze a single file
./code_stats.sh src/main.go

# Analyze a project with debug mode enabled (shows per-file details)
./code_stats.sh /path/to/project -d
```

## 🛠️ Supported Languages & Comment Symbols

| Language    | Common Extensions             | Comment Symbol |
|------------|------------------------------|---------------|
| Go         | `.go`                        | `//`          |
| Markdown   | `.md`                        | (N/A)         |
| Shell      | `.sh`, `.bash`, `.zsh`       | `#`           |
| YAML       | `.yml`, `.yaml`              | `极`          |
| Python     | `.py`                        | `#`           |
| C          | `.c`, `.h`                   | `//`          |
| C++        | `.cpp`, `.hpp`, `.cxx`       | `//`          |
| Java       | `.java`                      | `//`          |
| JavaScript | `.极s`, `.mjs`, `.jsx`       | `//`          |
| TypeScript | `.ts`, `.tsx`                | `//`          |
| HTML       | `.html`, `.htm`              | (N/A)         |
| CSS        | `.css`                       | (极/A)         |
| Ruby       | `.rb`                        | `#`           |
| Rust       | `.rs`                        | `//`          |
| PHP        | `.php`                       | `//`          |
| TOML       | `.toml`                      | `#`           |
| Dockerfile | `Dockerfile`                 | `#`           |
| Makefile   | `Makefile`                   | `#`           |

*Note: Markup languages (e.g., HTML, CSS, Markdown) typically don't have traditional comments, so only blank and content lines are counted.*

## 🔧 Ignored Patterns

The tool uses the `find` command for scanning and automatically excludes the following patterns to ensure analysis focuses on source code:

*   **Version Control & IDE Configs**: `*/.git/*`, `*/.idea/*`, `*/.vscode/*`
*   **Dependencies & Packages**: `*/node_modules/*`, `*/vendor/*`, `*/dist/*`, `*/build/*`, `*/target/*`
*   **Log & Lock Files**: `*.log`, `*.lock`
*   **Minified & Production Files**: `*.min.*`
*   **Image Assets**: `*.svg`, `*.png`, `*.jpg`
*   **Binary & Executable Files**: `*.so`, `*.dll`, `*.exe`, `*.bin`
*   **Editor Temporaries**: `*.swp`

## 📄 License

This project is open source under the MIT License. See the LICENSE file for details.
