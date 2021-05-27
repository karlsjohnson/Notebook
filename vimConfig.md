# Config

- [Mapping keys in Vim - Tutorial (Part 1)](https://vim.fandom.com/wiki/Mapping_keys_in_Vim_-_Tutorial_(Part_1))
- [Mapping keys in Vim - Tutorial (Part 2)](https://vim.fandom.com/wiki/Mapping_keys_in_Vim_-_Tutorial_(Part_2))
- [Mapping keys in Vim - Tutorial (Part 3)](https://vim.fandom.com/wiki/Mapping_keys_in_Vim_-_Tutorial_(Part_3))
- `:help key-notation` to find key options

**Re-mapping** shortcuts

- Add to .vimrc to:
  - Now just press Esc followed by confe to edit ~/.vimrc file.
  - To reload type Esc followed by confr.

```vim
" Edit vimr configuration file
nnoremap confe :e $MYVIMRC<CR>
" Reload vims configuration file
nnoremap confr :source $MYVIMRC<CR>
```

- Some people like to use the (Leader) key in a .vimrc file. So above mapping becomes:

```vim
" Edit vimr configuration file
nnoremap (Leader)ve :e $MYVIMRC<CR>
" " Reload vimr configuration file
nnoremap (Leader)vr :source $MYVIMRC<CR>
```

- The (Leader) key is mapped to \ by default.
  - So you just press \ followed by ve to edit the file.
  - To reload the ~/vimrc file you press \ followed by vr

- Listing **key maps**
  - Commands
    - You can display a list of existing key maps: `:maps`
    - :nmap - Display normal mode maps
    - :imap - Display insert mode maps
    - :vmap - Display visual and select mode maps :smap - Display select mode maps
    - :xmap - Display visual mode maps
    - :cmap - Display command-line mode maps :omap - Display operator pending mode maps
    - Add a key to display just one key (not for maps)
  - first column indicates the mode in which the map works
    - n Normal mode map. Defined using ':nmap' or ':nnorema
    - i Insert mode map. Defined using ':imap' or ':inorema
    - v Visual and select mode map. Defined using ':vmap' o
    - x Visual mode map. Defined using ':xmap' or ':xnorema
    - s Select mode map. Defined using ':smap' or ':snorema
    - c Command-line mode map. Defined using ':cmap' or ':c
    - o Operator pending mode map. Defined using ':omap' or
    - (Space) Normal, Visual and operator pending mode map. ':map' or ':noremap'.
    - ! Insert and command-line mode map. Defined using 'ma 'noremap!'.
  - The following characters may be displayed before the {rhs} of the map:
    - `*` The {rhs} of the map is not re-mappable. Defined us ':noremap' or ':nnoremap' or ':inoremap', etc. comm
    - & Only script local mappings are re-mappable in the {map. The map command has the (script) attribute.
    - @ A buffer local map command with the (buffer) attrib
  - Removing a keymap `unmap <F8>`
    - You can remove a mode-specific map by using the mode specific unmap command.
      - nunmap - Unmap a normal mode map
      - vunmap - Unmap a visual and select mode map
      - xunmap - Unmap a visual mode map
      - sunmap - Unmap a select mode map
      - iunmap - Unmap an insert and replace mode map
      - cunmap - Unmap a command-line mode map
      - ounmap - Unmap an operator pending mode map
  - Map Types
    - nnoremap - normal mode
    - inoremap - Insert and Replace
    - vnoremap - Visual and Select
    - xnoremap - Visual mode
    - snoremap - Select mode
    - cnoremap - Command-line mode
