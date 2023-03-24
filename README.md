<h1 align="center">
💾 NeoSave.nvim
</h1>

<p align="center">
  <a href="http://www.lua.org">
    <img
      alt="Lua"
      src="https://img.shields.io/badge/Lua-blue.svg?style=for-the-badge&logo=lua"
    />
  </a>
  <a href="https://neovim.io/">
    <img
      alt="Neovim"
      src="https://img.shields.io/badge/NeoVim-%2357A143.svg?&style=for-the-badge&logo=neovim&logoColor=white"
    />
  </a>
</p>

![demo](link-to-gif)

## 📢 Introduction

NeoSave is a Neovim plugin that automatically saves your files as you edit, ensuring your progress is preserved. Configure NeoSave to save either the current buffer or all open buffers, and easily toggle auto-saving on and off.

## ✨ Features

- Save all open buffers or only the current buffer.
- Auto-save files upon modification.
- Toggle auto-saving on and off.

## 💾 Persistence

NeoSave remembers the auto-save enabled state across sessions.

## 🛠️ Usage

To toggle NeoSave on and off, you can use the `ToggleNeoSave` command:

```vim
:ToggleNeoSave
```
You can also create a keybinding to toggle NeoSave more conveniently:

```lua
vim.keymap.set("n", "<leader>s", "<cmd>ToggleNeoSave<cr>", { noremap = true, silent = true })
```

## 📦 Installation

1. Install via your favorite package manager.

- [lazy.nvim](https://github.com/folke/lazy.nvim)
```lua
{
  "ecthelionvi/NeoSave.nvim",
  opts = {}
},
```

- [packer.nvim](https://github.com/wbthomason/packer.nvim)
```lua
use "ecthelionvi/NeoSave.nvim"
```

2. Setup the plugin in your `init.lua`. This step is not needed with lazy.nvim if `opts` is set as above.

```lua
require("NeoSave").setup()
```

## 🔧 Configuration

Pass your config table into the setup() function or opts with lazy.nvim.

The available options:

- `enabled` (boolean): enable or disable auto-saving by default
  - true (default)
- `write_all_bufs` (boolean): save all open buffers or only the current buffer
  - false (default)

### Default config

```Lua
local config = {
  enabled = true,
  write_all_bufs = false,
}
```
