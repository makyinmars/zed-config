# Zed Configuration

This repository contains my personal configuration for the [Zed Editor](https://zed.dev/). It includes customized keymaps, settings, and various optimizations for a Vim-like editing experience.

Higly inspired by [Jellydn Zed 101 Setup](https://github.com/jellydn/zed-101-setup)

## Features

### 🎨 Theme & Visual Settings
- Theme: Gruvbox Dark Hard
- Font: Berkeley Mono Variable (14px for both buffer and UI)
- Relative line numbers enabled
- Rainbow indent guides
- Hidden scrollbar
- Centered layout for zen mode
- Tab bar shows only errors

### ⌨️ Keybindings

#### Vim Mode
- Normal and Visual mode customizations
- Better escape sequences: `kj` and `jk` in insert mode
- Sneak motion support with `s` and `S`
- Window movement with `Ctrl + h/j/k/l`

#### Git Integration
- `space g h d`: Toggle selected diff hunks
- `space g s`: Toggle git panel
- `]h` / `[h`: Navigate between hunks
- Git panel docked to the left

#### LSP Features
- `space c a` or `space .`: Code actions
- `space c r`: Rename
- `gd`: Go to definition
- `gi`: Go to implementation
- `gt`: Go to type definition
- `gr`: Find all references
- `]d/[d`: Navigate diagnostics
- `space d e`: Show diagnostic hover
- `space d q`: Open diagnostics panel

#### File Navigation
- `space s f`: File finder
- `space e`: Toggle file explorer
- `space /`: Project search
- `space s w`: Search word under cursor

#### Panel Management
- `space |`: Split right
- `space _`: Split down
- `space w |`: Split right (prefix-based)
- `space w -`: Split down (prefix-based)
- `space w w`: Switch to other pane
- `space w d`: Close active pane
- `Ctrl + \`: Toggle terminal
- `escape escape`: Quick terminal exit
- `Cmd + b`: Toggle left dock

### 🤖 AI Integration
- Default AI: Claude Sonnet 4 Thinking (zed.dev)
- Agent profile configured with comprehensive tool access
- Ollama configuration included (commented)
- `space a a`: Toggle AI assistant
- `space a q`: Quote selection for AI
- Multiple AI profiles supported

### 🔧 Language Support

#### TypeScript/JavaScript
- Inlay hints configuration
- Custom LSP settings
- Tailwind CSS support

#### Python
- Ruff formatter
- Pyright integration
- Format on save enabled

### 📁 File Management
- Comprehensive file scan exclusions
- Custom file type associations
- Project panel with git status
- Outline panel docked to right

### 🔄 Code Folding (NEW)
- `space z a`: Toggle fold at cursor
- `space z o`: Unfold lines
- `space z c`: Fold all
- Neovim-consistent folding patterns

### 🔧 Neovim Consistency
This configuration maintains muscle memory consistency with Neovim LazyVim:
- Diagnostic navigation (`]d`/`[d`) matches exactly
- Window management (`space w` prefix) mirrors Neovim
- Insert mode escapes (`kj`/`jk`) work identically
- Code folding (`space z` prefix) follows Neovim conventions
- Space-based leader key system consistent across editors

## Installation

1. Clone this repository to your Zed config directory:
```bash
git clone https://github.com/makyinmars/zed-config ~/.config/zed
```

2. The configuration includes:
   - Enhanced keymap.json with Neovim-inspired patterns
   - Optimized settings.json for productivity
   - CLAUDE.md for AI assistant guidance
   - Comprehensive documentation

## Key Features

- **Neovim Consistency**: Maintains familiar keybinding patterns
- **Enhanced Diagnostics**: Improved workflow for error navigation
- **Code Folding**: Basic folding support with intuitive keybindings
- **AI Integration**: Advanced agent configuration with comprehensive tools
- **Window Management**: Efficient pane splitting and navigation
