# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Zed Editor configuration repository containing personal settings, keymaps, and customizations for a Vim-like editing experience. The configuration includes AI assistant integration, custom themes, and comprehensive keybindings.

## Key Configuration Files

- `settings.json` - Main Zed editor configuration with themes, AI settings, LSP configs, and language-specific settings
- `keymap.json` - Vim-style key bindings and custom shortcuts for navigation, LSP actions, and panel management
- `themes/` - Custom theme files (currently empty but available for theme extensions)
- `conversations/` - Zed AI conversation history files (`.zed.json` format)

## Important Configuration Details

### AI Integration
- Default AI model: `claude-sonnet-4-thinking` via `zed.dev` provider
- Agent profile configured as "write" with comprehensive tool access
- Ollama integration available but commented out (configured for `http://localhost:11434`)

### Editor Settings
- Vim mode enabled with relative line numbers
- Base keymap: VSCode compatibility
- Font: Berkeley Mono Variable (14px)
- Theme: Gruvbox Dark Hard
- Inlay hints disabled globally but configurable per language

### Language Support
- **Python**: Uses Ruff formatter and Pyright LSP, format on save enabled
- **TypeScript**: Inlay hints disabled, TailwindCSS language server configured
- Custom file type associations for Dockerfile and JSON variants

### Key Binding Patterns

#### Core Navigation
- Space-prefixed commands for major actions (`space g s` for git panel, `space a a` for AI)
- Vim-style navigation with `hjkl` and `Ctrl+hjkl` for pane movement
- LSP actions follow standard Vim conventions (`gd` for definition, `gr` for references)
- Terminal toggled with `Ctrl+\`

#### Enhanced Diagnostic Workflow (Neovim-inspired)
- `]d` / `[d` - Navigate next/previous diagnostic
- `space d e` - Show diagnostic float/hover
- `space d q` - Open diagnostics panel
- `space x x` - Deploy diagnostics panel

#### Window Management (Neovim-inspired)
- **Basic Splits**: `space |` (split right), `space _` (split down)  
- **Prefix-based**: `space w |` (split right), `space w -` (split down)
- **Window Control**: `space w w` (switch pane), `space w d` (close pane)
- **Pane Navigation**: `Ctrl+hjkl` for directional movement

#### Code Folding (Neovim-inspired)
- `space z a` - Toggle fold at cursor
- `space z o` - Unfold lines  
- `space z c` - Fold all
- Note: Folding in Zed is currently basic compared to Neovim

#### Terminal Enhancements
- `Ctrl+\` - Toggle terminal panel
- `escape escape` - Quick terminal exit (in terminal context)
- `Ctrl+hjkl` - Navigate between panes from terminal

#### Insert Mode
- `kj` / `jk` - Escape to normal mode (consistent with Neovim)

## Development Commands

This is a configuration repository, so there are no build/test commands. Configuration changes take effect immediately in Zed Editor.

To validate configuration:
- JSON files are automatically validated by Zed's JSON language server
- Invalid keymap bindings will show errors in Zed's command palette

## Neovim Consistency

This configuration maintains consistency with Neovim LazyVim patterns:
- **Diagnostic Navigation**: `]d`/`[d` pattern matches exactly
- **Window Management**: `space w` prefix system mirrors Neovim window commands
- **Insert Mode Escapes**: `kj`/`jk` escape sequences work identically
- **Code Folding**: `space z` prefix follows Neovim folding conventions
- **Leader Key Patterns**: Space-based leader key system consistent across both editors

## Key Binding Reference

### Commonly Used Shortcuts
- `space space` - File/buffer switcher
- `space s f` - File finder
- `space /` - Project search
- `space e` - Toggle/reveal project panel
- `space g s` - Git panel
- `space a a` - AI assistant
- `space r t` - Run nearest task

### Buffer Management  
- `shift h/l` - Previous/next buffer
- `space b d` - Close buffer
- `space b o` - Close other buffers

## Architecture Notes

- Configuration follows Zed's standard structure with separate concerns (settings vs keymaps)
- Agent configuration enables comprehensive tooling for AI-assisted development
- File scan exclusions prevent noise from build artifacts and dependencies
- Panel layout optimized for left-side git/project panels, right-side outline
- Keymap organization prioritizes muscle memory consistency with Neovim