# Zed Configuration

This repository contains my personal configuration for the [Zed Editor](https://zed.dev/). It includes customized keymaps, settings, and various optimizations for a Vim-like editing experience.

Higly inspired by [Jellydn Zed 101 Setup](https://github.com/jellydn/zed-101-setup)

## Features

### 🎨 Theme & Visual Settings
- Theme: Tokyo Night
- Font: Berkeley Mono Variable (15px for buffer, 16px for UI)
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

#### File Navigation
- `space s f`: File finder
- `space e`: Toggle file explorer
- `space /`: Project search
- `space s w`: Search word under cursor

#### Panel Management
- `space |`: Split right
- `space _`: Split down
- `Ctrl + \`: Toggle terminal
- `Cmd + b`: Toggle left dock

### 🤖 AI Integration
- Default AI: Claude 3 Sonnet (zed.dev)
- Ollama configuration included (commented)
- `space a a`: Toggle AI assistant
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

## Installation

1. Clone this repository to your Zed config directory:
```bash
git clone https://github.com/makyinmars/zed-config ~/.config/zed
