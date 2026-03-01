Neovim Configuration

A modern Neovim configuration with LSP support, fuzzy finding, and productivity-focused keybindings.

## Install
- you will need to make clone this down to a config folder, which is hidden on some os's such as ubuntu,
make sure you run ls -a to show hidden folders
- after you add it into the config folder run `nvim` in your terminal to open the neovim then `:PackerSync` command. This should download everything you need. 

## 📁 File Structure

```
nvim/
├── init.lua                 # Main entry point
├── lua/
│   └── wruqe/
│       ├── init.lua         # Module initialization
│       ├── set.lua          # Editor settings
│       ├── remap.lua        # Key mappings
│       └── packer.lua       # Plugin definitions
├── after/
│   └── plugin/              # Plugin-specific configurations
│       ├── telescope.lua    # Telescope keybindings
│       ├── harpoon.lua      # Harpoon configuration
│       ├── lsp.lua          # LSP setup
│       ├── treesitter.lua   # Treesitter config
│       ├── fugitive.lua     # Git integration
│       ├── undotree.lua     # Undo tree
│       └── colors.lua       # Color scheme
└── plugin/
    └── packer_compiled.lua  # Packer compiled file
```

## ⌨️ Keybindings

### Leader Key

- `<leader>` = `Space`

### File Operations

- `<leader>pv` - Open file explorer (netrw)
- `<leader>pf` - Find files (Telescope)
- `<C-p>` - Find git files (Telescope)
- `<leader>ps` - Grep string search (Telescope)
- `<leader>x` - Make current file executable

### Navigation

- `J` - Join lines (keeps cursor position)
- `K` - Move visual selection up
- `J` (visual) - Move visual selection down
- `<C-d>` - Scroll down (centers cursor)
- `<C-u>` - Scroll up (centers cursor)
- `n` - Next search result (centers cursor)
- `N` - Previous search result (centers cursor)

### Quickfix & Location Lists

- `<C-k>` - Next quickfix item
- `<C-j>` - Previous quickfix item
- `<leader>k` - Next location list item
- `<leader>j` - Previous location list item

### Harpoon (File Navigation)

- `<leader>a` - Add file to harpoon
- `<C-e>` - Toggle harpoon quick menu
- `<C-h>` - Navigate to harpoon file 1
- `<C-t>` - Navigate to harpoon file 2
- `<C-n>` - Navigate to harpoon file 3
- `<C-s>` - Navigate to harpoon file 4
- `<C-S-P>` - Previous harpoon file
- `<C-S-N>` - Next harpoon file

### LSP (Language Server Protocol)

- `gd` - Go to definition
- `K` - Hover documentation
- `<leader>vws` - Workspace symbol
- `<leader>vd` - Open diagnostic float
- `[d` - Next diagnostic
- `]d` - Previous diagnostic
- `<leader>vca` - Code actions
- `<leader>vrr` - References
- `<leader>vrn` - Rename
- `<C-h>` (insert) - Signature help
- `<leader>f` - Format buffer

### Copy/Paste

- `<leader>p` (visual) - Paste without yanking (greatest remap ever)
- `<leader>y` - Yank to system clipboard
- `<leader>Y` - Yank line to system clipboard
- `<leader>d` - Delete to void register (don't yank)

### Search & Replace

- `<leader>s` - Search and replace word under cursor

### Code Snippets

- `<leader>ee` - Insert Go error handling block

### Utility

- `<leader><leader>` - Source current file
- `<C-c>` (insert) - Escape to normal mode
- `Q` - Disabled (no ex mode)
- `<C-f>` - Open tmux sessionizer
- `<leader>mr` - Make it rain (Cellular Automaton)
- `<leader>vwm` - Start Vim With Me
- `<leader>svwm` - Stop Vim With Me

## 🔌 Plugins

### Core Plugins

- **Packer** - Plugin manager
- **Telescope** - Fuzzy finder
- **Treesitter** - Syntax highlighting
- **Harpoon** - File navigation
- **LSP-Zero** - LSP configuration
- **nvim-cmp** - Autocompletion

### UI & Colors

- **Rose Pine** - Color scheme

### Git

- **vim-fugitive** - Git integration

### Utilities

- **undotree** - Undo history visualization
- **Treesitter Playground** - Treesitter exploration

## ⚙️ Editor Settings

- **Line Numbers**: Absolute + Relative
- **Tab Settings**: 4 spaces, expand tabs
- **Undo**: Persistent undo files
- **Search**: Incremental search, no highlight
- **Colors**: True color support
- **Scroll**: 8 line offset
- **Color Column**: 80 characters

## 🚀 Setup Instructions

### Prerequisites

1. **Neovim** (0.8+)
2. **ripgrep** (for Telescope grep)
   ```bash
   brew install ripgrep  # macOS
   # or
   sudo apt install ripgrep  # Linux
   ```
3. **Node.js** (for LSP servers)

### Installation

1. Clone this repository to your Neovim config directory:

   ```bash
   git clone <your-repo> ~/.config/nvim
   ```

2. Install Packer (if not already installed):

   ```bash
   git clone --depth 1 https://github.com/wbthomason/packer.nvim \
     ~/.local/share/nvim/site/pack/packer/start/packer.nvim
   ```

3. Open Neovim and install plugins:

   ```bash
   nvim
   :PackerSync
   ```

4. Install LSP servers (via Mason, which is included):
   - LSP servers will be installed automatically on first use
   - Or manually via `:Mason` command

## 📝 LSP Servers Configured

- TypeScript (`ts_ls`)
- ESLint (`eslint`)
- Lua (`lua_ls`)
- Rust (`rust_analyzer`)
- Python (`basedpyright`)

## 🎨 Color Scheme

This configuration uses **Rose Pine** as the default color scheme. You can change it in `lua/wruqe/packer.lua`.

## 🔧 Customization

- **Keybindings**: Edit `lua/wruqe/remap.lua`
- **Settings**: Edit `lua/wruqe/set.lua`
- **Plugins**: Edit `lua/wruqe/packer.lua`
- **Telescope**: Edit `after/plugin/telescope.lua`
- **Harpoon**: Edit `after/plugin/harpoon.lua`
- **LSP**: Edit `after/plugin/lsp.lua`

## 📚 Resources

- [Neovim Documentation](https://neovim.io/doc/)
- [Telescope](https://github.com/nvim-telescope/telescope.nvim)
- [Harpoon](https://github.com/ThePrimeagen/harpoon)
- [LSP-Zero](https://github.com/VonHeikemen/lsp-zero.nvim)

## 📄 License

This configuration is for personal use. Feel free to fork and modify for your needs.
