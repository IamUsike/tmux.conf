# 🚀 ZSH Configuration Cheat Sheet

## 📋 Table of Contents

- [Key Bindings](#key-bindings)
- [File Operations](#file-operations)
- [Directory Navigation](#directory-navigation)
- [Git Commands](#git-commands)
- [System Management](#system-management)
- [Development Tools](#development-tools)
- [Docker Commands](#docker-commands)
- [Package Management](#package-management)
- [Custom Functions](#custom-functions)
- [FZF Integration](#fzf-integration)
- [Oh My Zsh Plugins](#oh-my-zsh-plugins)

---

## ⌨️ Key Bindings

| Key Combination | Action                        |
| --------------- | ----------------------------- |
| `Ctrl + R`      | Fuzzy history search (FZF)    |
| `Ctrl + T`      | Fuzzy file finder (FZF)       |
| `Alt + C`       | Fuzzy directory changer (FZF) |
| `Ctrl + →`      | Move forward one word         |
| `Ctrl + ←`      | Move backward one word        |
| `↑/↓`           | History substring search      |
| `Tab`           | Enhanced completion with menu |

---

## 📁 File Operations

### Basic File Commands

| Alias | Command         | Description                      |
| ----- | --------------- | -------------------------------- |
| `ls`  | `lsd`           | Enhanced ls with icons           |
| `l`   | `ls -l`         | Long format listing              |
| `la`  | `ls -a`         | Show hidden files                |
| `lla` | `ls -la`        | Long format with hidden files    |
| `lt`  | `ls --tree`     | Tree view                        |
| `llt` | `ls -la --tree` | Long tree view with hidden files |

### Safe File Operations

| Alias   | Command     | Description                 |
| ------- | ----------- | --------------------------- |
| `cp`    | `cp -iv`    | Interactive, verbose copy   |
| `mv`    | `mv -iv`    | Interactive, verbose move   |
| `rm`    | `rm -iv`    | Interactive, verbose remove |
| `mkdir` | `mkdir -pv` | Create parent dirs, verbose |

### Custom File Functions

| Function  | Usage                 | Description                     |
| --------- | --------------------- | ------------------------------- |
| `mkcd`    | `mkcd dirname`        | Create directory and cd into it |
| `backup`  | `backup file.txt`     | Create file.txt.bak             |
| `extract` | `extract archive.zip` | Extract any archive format      |
| `ff`      | `ff filename`         | Find files by name              |
| `fd`      | `fd dirname`          | Find directories by name        |

---

## 🗂️ Directory Navigation

| Alias   | Command          | Description              |
| ------- | ---------------- | ------------------------ |
| `..`    | `cd ..`          | Go up one directory      |
| `...`   | `cd ../..`       | Go up two directories    |
| `....`  | `cd ../../..`    | Go up three directories  |
| `.....` | `cd ../../../..` | Go up four directories   |
| `~`     | `cd ~`           | Go to home directory     |
| `-`     | `cd -`           | Go to previous directory |

**Note**: `cd` is enhanced with `zoxide` for smart directory jumping based on frequency and recency.

---

## 🔧 Git Commands

### Basic Git Operations

| Alias | Command              | Description                     |
| ----- | -------------------- | ------------------------------- |
| `ga`  | `git add .`          | Add all files                   |
| `gaa` | `git add --all`      | Add all files including deleted |
| `gc`  | `git commit`         | Commit changes                  |
| `gcm` | `git commit -m`      | Commit with message             |
| `gca` | `git commit --amend` | Amend last commit               |
| `gp`  | `git push`           | Push to remote                  |
| `gpl` | `git pull`           | Pull from remote                |

### Git Information

| Alias | Command                                | Description      |
| ----- | -------------------------------------- | ---------------- |
| `gs`  | `git status`                           | Show status      |
| `gd`  | `git diff`                             | Show differences |
| `gl`  | `git log --oneline --graph --decorate` | Pretty log       |
| `gb`  | `git branch`                           | List branches    |

### Git Navigation

| Alias | Command           | Description                |
| ----- | ----------------- | -------------------------- |
| `gco` | `git checkout`    | Checkout branch/commit     |
| `gcb` | `git checkout -b` | Create and checkout branch |
| `gm`  | `git merge`       | Merge branch               |

### Git Utilities

| Alias  | Command         | Description         |
| ------ | --------------- | ------------------- |
| `gr`   | `git reset`     | Reset changes       |
| `gst`  | `git stash`     | Stash changes       |
| `gstp` | `git stash pop` | Pop stashed changes |

### Custom Git Functions

| Function      | Usage               | Description                 |
| ------------- | ------------------- | --------------------------- |
| `gclone`      | `gclone <repo-url>` | Clone and cd into repo      |
| `fzf_git_log` | `fzf_git_log`       | Interactive git log browser |

---

## 🖥️ System Management

### System Information

| Alias   | Command               | Description                 |
| ------- | --------------------- | --------------------------- |
| `df`    | `df -h`               | Disk usage (human readable) |
| `du`    | `du -h`               | Directory usage             |
| `free`  | `free -h`             | Memory usage                |
| `ps`    | `ps auxf`             | Process tree                |
| `psg`   | `ps aux \| grep`      | Search processes            |
| `myip`  | `curl -s ifconfig.me` | Show public IP              |
| `ports` | `netstat -tulanp`     | Show open ports             |

### System Control

| Alias  | Command            | Description    |
| ------ | ------------------ | -------------- |
| `sctl` | `sudo systemctl`   | System control |
| `jctl` | `journalctl`       | Journal logs   |
| `uctl` | `systemctl --user` | User services  |

### Custom System Functions

| Function   | Usage            | Description                    |
| ---------- | ---------------- | ------------------------------ |
| `sysup`    | `sysup`          | Update system and AUR packages |
| `killport` | `killport 3000`  | Kill process on port 3000      |
| `weather`  | `weather London` | Get weather info               |
| `fzf_kill` | `fzf_kill`       | Interactive process killer     |

---

## 💻 Development Tools

### Editor Shortcuts

| Alias  | Command  | Description                  |
| ------ | -------- | ---------------------------- |
| `nv`   | `nvim`   | Neovim                       |
| `vim`  | `nvim`   | Neovim (vim replacement)     |
| `vi`   | `nvim`   | Neovim (vi replacement)      |
| `code` | `code .` | VS Code in current directory |

### Config File Shortcuts

| Alias    | Command                        | Description        |
| -------- | ------------------------------ | ------------------ |
| `zshrc`  | `nvim ~/.zshrc`                | Edit zsh config    |
| `tmuxrc` | `nvim ~/.tmux.conf`            | Edit tmux config   |
| `nvimrc` | `nvim ~/.config/nvim/init.lua` | Edit neovim config |

### Python & Development

| Alias   | Command                  | Description            |
| ------- | ------------------------ | ---------------------- |
| `py`    | `python3`                | Python 3               |
| `pip`   | `pip3`                   | Python package manager |
| `serve` | `python3 -m http.server` | Quick HTTP server      |
| `json`  | `python3 -m json.tool`   | Pretty print JSON      |

---

## 🐳 Docker Commands

| Alias    | Command                       | Description             |
| -------- | ----------------------------- | ----------------------- |
| `Docker` | `sudo systemctl start docker` | Start Docker service    |
| `dps`    | `docker ps`                   | List running containers |
| `dpsa`   | `docker ps -a`                | List all containers     |
| `di`     | `docker images`               | List images             |
| `drm`    | `docker rm`                   | Remove container        |
| `drmi`   | `docker rmi`                  | Remove image            |
| `dstop`  | `docker stop $(docker ps -q)` | Stop all containers     |
| `dclean` | `docker system prune -af`     | Clean up Docker system  |

---

## 📦 Package Management (Arch Linux)

### Pacman Commands

| Alias     | Command            | Description         |
| --------- | ------------------ | ------------------- |
| `pacup`   | `sudo pacman -Syu` | Update system       |
| `pacin`   | `sudo pacman -S`   | Install package     |
| `pacre`   | `sudo pacman -R`   | Remove package      |
| `pacse`   | `pacman -Ss`       | Search packages     |
| `pacinfo` | `pacman -Si`       | Package information |

### AUR Helper (Yay)

| Alias   | Command    | Description         |
| ------- | ---------- | ------------------- |
| `yayup` | `yay -Syu` | Update AUR packages |
| `yayin` | `yay -S`   | Install AUR package |

---

## 🔍 Custom Functions

### Utility Functions

| Function   | Usage                   | Description               |
| ---------- | ----------------------- | ------------------------- |
| `note`     | `note "Remember to..."` | Add quick note            |
| `notes`    | `notes`                 | View all notes            |
| `path`     | `path`                  | Show PATH variable nicely |
| `now`      | `now`                   | Current time              |
| `nowdate`  | `nowdate`               | Current date              |
| `help-zsh` | `help-zsh`              | Show this help            |

---

## 🔎 FZF Integration

### FZF Key Bindings

- **Ctrl+R**: Fuzzy history search
- **Ctrl+T**: Fuzzy file finder
- **Alt+C**: Fuzzy directory changer

### Custom FZF Functions

| Function      | Description                      |
| ------------- | -------------------------------- |
| `fzf_git_log` | Interactive git log with preview |
| `fzf_kill`    | Interactive process killer       |

### FZF Environment Variables

\`\`\`bash
FZF_DEFAULT_OPTS="--height 40% --layout=reverse --border --inline-info"
FZF_DEFAULT_COMMAND='fd --type f --hidden --follow --exclude .git'
\`\`\`

---

## 🔌 Oh My Zsh Plugins

### Active Plugins

| Plugin                    | Description                            |
| ------------------------- | -------------------------------------- |
| `git`                     | Git aliases and functions              |
| `archlinux`               | Arch Linux specific commands           |
| `zsh-autosuggestions`     | Command suggestions based on history   |
| `zsh-syntax-highlighting` | Syntax highlighting for commands       |
| `colored-man-pages`       | Colorized man pages                    |
| `command-not-found`       | Suggests packages for missing commands |
| `extract`                 | Universal archive extractor            |
| `web-search`              | Web search from terminal               |
| `copypath`                | Copy current path to clipboard         |
| `copyfile`                | Copy file contents to clipboard        |
| `dirhistory`              | Navigate directory history             |
| `sudo`                    | Double ESC to add sudo                 |

### Plugin-Specific Commands

#### Web Search Plugin

- `google <query>` - Search Google
- `github <query>` - Search GitHub
- `stackoverflow <query>` - Search Stack Overflow

#### Extract Plugin

- `extract <archive>` - Extract any supported archive

#### Directory History Plugin

- `Alt + ←` - Previous directory
- `Alt + →` - Next directory
- `Alt + ↑` - Parent directory

---

## 🎨 Customization

### Theme

- **Current**: `gentoo` theme
- **Location**: `~/.oh-my-zsh/themes/`

### Custom Prompt Elements

The gentoo theme shows:

- Username and hostname
- Current directory
- Git branch and status
- Command execution time
- Exit status indicator

### Environment Variables

\`\`\`bash
EDITOR='nvim' # Default editor
VISUAL='nvim' # Visual editor
BROWSER='firefox' # Default browser
TERMINAL='alacritty' # Default terminal
\`\`\`

---

## 🚀 Quick Start Tips

1. **Type `help-zsh`** for a quick reference anytime
2. **Use Tab completion** extensively - it's enhanced with menu selection
3. **Try Ctrl+R** for fuzzy history search instead of arrow keys
4. **Use `mkcd dirname`** instead of `mkdir dirname && cd dirname`
5. **Try `weather <city>`** for quick weather info
6. **Use `sysup`** for complete system updates
7. **Remember `backup filename`** before editing important files

---

## 📝 Notes System

- `note "your note here"` - Add a timestamped note
- `notes` - View all your notes
- Notes are stored in `~/notes.txt`

---

_This configuration enhances your terminal experience with productivity shortcuts, better navigation, and powerful search capabilities. Enjoy your enhanced ZSH setup! 🎉_
