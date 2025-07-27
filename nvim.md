# Kickstart.nvim Cheat‑Sheet

## Leader Keys
| Key | Purpose |
|-----|---------|
| `SPACE` | **Leader** (`<leader>`) |
| `SPACE` | **Local‑leader** (`<localleader>`) |

## Basic Normal‑Mode Keymaps
| Keys | Action |
|------|--------|
| `<Esc>` | Clear search highlights |
| `<leader>q` | Open diagnostics **Q**uickfix list |
| `Ctrl‑h / j / k / l` | Move focus to split **h/j/k/l** |
| Arrow keys | Disabled → hints to use *hjkl* |
| `<Esc><Esc>` (terminal) | Leave terminal‑insert mode |


## Indenting & Alignment
| Mode | Right › | Left ‹ | Notes |
|------|---------|--------|-------|
| Normal | `>>` | `<<` | Count works: `5>>` indents 5 lines |
| Visual | `>` | `<` | Acts on selection |
| Insert | `<C-t>` | `<C-d>` | Shift one *shiftwidth* while editing |
| Visual (mapping) | **`<Tab>`** | **`<S-Tab>`** | Shifts & keeps selection (`>gv` / `<gv`) |

## Comment / Uncomment  *(mini.comment)*
| Mode | Toggle | Result |
|------|--------|--------|
| Normal | `gcc` | Comment / uncomment current line |
| Visual | `gc` | Toggle selected lines |
| Visual | `gC` | **Only** comment selection |
| *(Optional mapping)* | `<leader>/` | Same as `gcc` / `gc` |

## Formatting
| Keys | Scope | Formatter |
|------|-------|-----------|
| `<leader>f` | Buffer | **Conform.nvim** (LSP fallback) |
| `<leader>gf` | Buffer (Go) | `goimports → gofumpt` (if configured) |

## Completion (blink.cmp “default” preset)
| Keys | Action |
|------|--------|
| `<C-y>` | Accept completion / expand snippet |
| `<Tab>` / `<S-Tab>` | Jump **forward / back** inside snippet |
| `<C-n>` / `<C-p>` `↑` / `↓` | Next / previous menu item |
| `<C-space>` | Open menu / show docs |
| `<C-k>` | Toggle signature-help popup |
| `<C-e>` | Hide completion menu |


## Telescope Shortcuts
| Keys | Picker |
|------|--------|
| `<leader>sh` | Help tags |
| `<leader>sk` | Keymaps |
| `<leader>sf` | Files |
| `<leader>s.` | Recent files |
| `<leader>sw` | Grep current word |
| `<leader>sg` | Live grep |
| `<leader>sd` | Diagnostics |
| `<leader>s/` | Live grep in open files |
| `<leader>s,` | Resume last picker |
| `<leader>/`  | Fuzzy search buffer |
| `<leader>sn` | Search *nvim* config |

## LSP Essentials
| Keys | Description |
|------|-------------|
| `grd` | Goto **D**efinition |
| `grr` | References |
| `gri` | Implementation |
| `grt` | Type definition |
| `grD` | Declaration |
| `grn` | Rename |
| `gra` | Code action |
| `gO` | Document symbols |
| `gW` | Workspace symbols |
| `<leader>th` | Toggle inlay hints |

Diagnostics: sign column always visible, severity‑sorted.

## Toggles & Utilities
| Keys | Action |
|------|--------|
| `<leader>e` | Toggle **oil** file explorer |
| `<leader>f` | Format buffer |
| `<space>sh` | Search help |

## Plugin Manager – lazy.nvim
| Command | Purpose |
|---------|---------|
| `:Lazy` | Plugin UI |
| `:Lazy update` | Update plugins |

## Core Options
* Line numbers + **relative** numbers  
* Mouse enabled  
* Clipboard sync (`unnamedplus`)  
* Undo history persisted  
* Smart‑case search  
* Break indent, sign column on  
* Splits open right/below  
* Cursorline, `scrolloff` 10  
* Visible whitespace (`» `, `·`, `␣`)  
* Fast UI (`updatetime=250`, `timeoutlen=300`)

## First‑Run Tips
```vim
:Tutor          " learn movement
:help           " intro help
:Lazy           " plugin manager
:checkhealth    " diagnose setup
