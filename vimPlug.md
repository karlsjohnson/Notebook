# Plugins

## vim-plug

[vim-plug](https://github.com/junegunn/vim-plug), A plugin manager

| Command                           | Description                       |
| :-------------------------------- | :-------------------------------- |
| PlugInstall [name ...] [threads] | Install plugins                   |
| PlugUpdate [name ...] [threads]  | Install or update plugins         |
| PlugClean[!]                      | Remove unlisted plugins           |
| PlugUpgrade                       | Upgrade vim-plug itself           |
| PlugStatus                        | Check the status of plugins       |
| PlugDiff                          | Examine changes from the previous |
| PlugSnapshot[!] [output path]     | Generate script for restoring     |

## nerdtree

_Program-VIM-Plugins:_ [preservim/nerdtree](https://github.com/preservim/nerdtree)

- Add keyboard shortcut Toggle View: `map <C-n> :NERDTreeToggle<CR>`
- open a NERDTree automatically: `autocmd vimenter * NERDTree`
- NERDTree automatically when vim starts up if no files:

```bash
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif
```

- close vim if the only window left open is a NERDTree `autocmd bufenter * if (winnr("$") == 1 && exists("b:NERDTree") && b:NERDTree.isTabTree()) | q | endif`

### VP markdown

- [(plasticboy)vim-markdown](https://github.com/plasticboy/vim-markdown)
- [tabular](https://github.com/godlygeek/tabular)
- Install via vim-plug
  - Install tabular first `Plug 'godlygeek/tabular'`
  - Install markdown `Plug 'plasticboy/vim-markdown'`
- new list item: (enter, A enter)
- new list item indent: (esc, o)

vim-markdown **Commands**
| Command      | Description                      |
|:-------------|:---------------------------------|
|              | ==Folding==                      |
| zr           | open one fold                    |
| zR           | opens all folds                  |
| zm           | close one fold                   |
| zM           | close all folds                  |
| za           | open fold at cursor              |
| zA           | open fold at cursor recursively  |
| zc           | close fold at cursor             |
| zC           | close fold at cursor recursively |
| gx           | open link at cursor in browser   |
| ge           | open link at cursor in vim       |
| ]]           | go to next header                |
| \[\[         | go to previous header            |
| \]\[         | go to next sibling header        |
| \[\]         | go to previous sibling header    |
| ]c           | go to Current header             |
| ]u           | go to parent header              |
| :TableFormat | Format table under cursor        |
| :Toc         | Create Toc Sidebar               |
| :Toch        | Create Toc below                 |
| :Toct        | Create Toc new tab               |

### fzf

- Links for plugins used
  - [fzf - fuzzy finder](ttps://github.com/junegunn/fzf.vim)
  - [fzf.vim](https://github.com/junegunn/fzf.vim)
  - [the_silver_searcher](https://github.com/ggreer/the_silver_searcher)
- vimrc
  - Change shortcut to Control-P: `nmap <C-P> :FZF<CR>`
    - Use to open any file under working directory
    - use `cd` to change working directory
  - fzf.vim shortcuts
    - Files (runs $FZF_DEFAULT_COMMAND if defined) `:Files [PATH]`
      - open any file under path
    - ag search result (ALT-A to select all, ALT-D to deselect all): `:Ag [PATTERN]`
      - the_silver_searcher is used here
      - Bang-versions of the commands (e.g. Ag!) will open fzf in fullscreen
    - Lines in loaded buffers: `:Lines [QUERY]`
    - Lines in the current buffer: `:BLines [QUERY]`
  - Most commands support CTRL-T / CTRL-X / CTRL-V key bindings to open in a new tab, a new split, or in a new vertical split

### VP comfortable-motion

- [comfortable-motion](https://github.com/yuttie/comfortable-motion.vim)
  - Brings physics-based smooth scrolling to the Vim/Neovim world!

### More

Looking at **Plugins** Look

- [ryanoasis/vim-devicons](https://github.com/ryanoasis/vim-devicons)
  - Adds file type icons to Vim plugins such as: NERDTree
- [neoclide/coc.nvim](https://github.com/neoclide/coc.nvim)
  - code completion
- [vim-airline/vim-airline](https://github.com/vim-airline/vim-airline)
  - status/tabline
- [reedes/vim-pencil](https://github.com/reedes/vim-pencil)
- [majutsushi/tagbar](https://github.com/majutsushi/tagbar)
  - displays tags in a window, ordered by scope
- [kien/ctrlp.vim](https://github.com/kien/ctrlp.vim)
- [wincent/command-t](https://github.com/wincent/Command-T)
- [vim-ctrlspace](https://github.com/vim-ctrlspace/vim-ctrlspace)
- [vim-signature](https://github.com/kshenoy/vim-signature)
- Pandoc
  - [vim-pandoc](https://github.com/vim-pandoc/vim-pandoc)
  - [vim-pandoc-syntax](https://github.com/vim-pandoc/vim-pandoc-syntax)
- Livedown (Preview)
  - [vim-livedown](https://github.com/shime/vim-livedown)
- [markdown-drawer](https://github.com/Scuilion/markdown-drawer)
- [vim-table-mode](https://github.com/dhruvasagar/vim-table-mode)
- [vim-marked](https://github.com/itspriddle/vim-marked)
- [mkdx](https://github.com/SidOfc/mkdx)
- [vim-markdown-folding](https://github.com/masukomi/vim-markdown-folding)
- [vim-pencil](https://github.com/reedes/vim-pencil)
