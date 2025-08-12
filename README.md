# TMUX Configuration Cheat Sheet

## Prefix Key

- **Prefix**: `Ctrl + Space`

## Session Management

| Shortcut     | Action                                   |
| ------------ | ---------------------------------------- |
| `prefix + S` | Create new session                       |
| `Alt + s`    | Choose session (interactive)             |
| `Alt + (`    | Switch to previous session               |
| `Alt + )`    | Switch to next session                   |
| `prefix + X` | Kill current session (with confirmation) |
| `prefix + d` | Detach from session                      |

## Window Management

| Shortcut     | Action                                   |
| ------------ | ---------------------------------------- |
| `prefix + c` | Create new window (in current directory) |
| `Alt + 1-5`  | Switch to window 1-5 directly            |
| `prefix + n` | Next window                              |
| `prefix + p` | Previous window                          |
| `prefix + <` | Swap window left                         |
| `prefix + >` | Swap window right                        |
| `prefix + ,` | Rename window                            |
| `prefix + &` | Kill window                              |

## Pane Management

| Shortcut           | Action                          |
| ------------------ | ------------------------------- |
| `prefix + \|`      | Split pane vertically           |
| `prefix + -`       | Split pane horizontally         |
| `Alt + Arrow Keys` | Switch panes (no prefix needed) |
| `prefix + h/j/k/l` | Switch panes (Vim-style)        |
| `prefix + H/J/K/L` | Resize panes (hold for repeat)  |
| `prefix + z`       | Toggle pane zoom                |
| `prefix + x`       | Kill pane                       |
| `prefix + b`       | Break pane to new window        |
| `prefix + j`       | Join pane from another window   |

## Copy Mode & Selection

| Shortcut     | Action                             |
| ------------ | ---------------------------------- |
| `prefix + [` | Enter copy mode                    |
| `v`          | Start selection (in copy mode)     |
| `Ctrl + v`   | Rectangle selection (in copy mode) |
| `y`          | Copy selection to clipboard        |
| `Enter`      | Copy selection and exit copy mode  |
| `prefix + /` | Search in copy mode                |
| `q`          | Exit copy mode                     |

## Utility Commands

| Shortcut            | Action                   |
| ------------------- | ------------------------ |
| `prefix + r`        | Reload tmux config       |
| `prefix + e`        | Edit tmux config in nvim |
| `prefix + Ctrl + l` | Clear pane history       |
| `prefix + t`        | Show clock               |
| `prefix + ?`        | Show all key bindings    |

## Mouse Support

- **Enabled**: Click to select panes, drag to resize, scroll to navigate history
- **Copy**: Select text with mouse, automatically copies to clipboard

## Status Bar Indicators

| Symbol | Meaning              |
| ------ | -------------------- |
| `󰠠`    | Prefix key is active |
| `󰍉`    | Pane is zoomed       |
| `󰏫`    | Window has activity  |
| `󰓎`    | Current window       |
| `󰍴`    | Last window          |

## Configuration Features

- **Base Index**: Windows and panes start at 1 (not 0)
- **Auto Renumber**: Windows automatically renumber when closed
- **History**: 50,000 lines of scrollback
- **Escape Time**: Reduced to 0ms for better Vim experience
- **Mouse**: Full mouse support enabled
- **Clipboard**: Integrated with system clipboard (Wayland)

## Color Scheme

- **Theme**: Nord-inspired color palette
- **Active Pane**: Cyan border (`#88c0d0`)
- **Inactive Pane**: Gray border (`#4c566a`)
- **Status Bar**: Dark gray background (`#3b4252`)
- **Current Window**: Cyan background (`#88c0d0`)

## Tips

1. **Vim Users**: All navigation uses Vim-style keys (h/j/k/l)
2. **Quick Access**: Alt+number keys work without prefix
3. **Directory Aware**: New panes/windows open in current directory
4. **Persistent**: Use plugins like tmux-resurrect to save sessions
5. **Customizable**: Edit config with `prefix + e` for quick changes

## External Commands

\`\`\`bash

# Start new session

tmux new-session -s session_name

# Attach to session

tmux attach-session -t session_name

# List sessions

tmux list-sessions

# Kill session

tmux kill-session -t session_name
