# How to add full support for a language in my Neovim config

1. Add it to the `ensure_installed` table in `treesitter.lua` (Not necessary, now it automatically installs the parser if it doesn't recognize the language).
2. Add its LSP (Language Server Protocol) in the `ensure_installed` table in `lsp-config.lua`.
3. Call its setup function within the `config` function for `nvim-lspconfig`.
4. Add its formatter to the sources table in `none-ls.lua`.
5. Install its formatter and linter in Mason.
6. Install its debugger (If necessary).
