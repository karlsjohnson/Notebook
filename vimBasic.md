# Basic

- **CLI commands**
  - Open vim with session *article*: `vim -S ~/.vim/sessions/article.vim`
- **Open and search** items
  - To open file and go to function called main(), enter:
  - $ vim +/main filename-here
  - You can use wildcards with the :edit command. So, `:e **/test/Suite.java`
  - :e command should have tab complete
  - The vi / vim text editor supports running any : command using the following syntax:
    - vi +commandHere fileName
    - vim +LineNumber fileName
    - vi +/searchTermHere fileName
    - vi +/LineNumberHere fileName
    - vim +/LineNumberHere fileName
  - To open file and go to function called main(), enter:
    - vim +/main filename-here
  - Next open file and go to line number 42, enter:
    - $ vim +42 fileName
  - [Open File And Go To Specific...](https://www.cyberciti.biz/faq/linux-unix-command-open-file-linenumber-function/)
- **Copy/Paste**
  - Yank(Copy), Delete(Cut) and Put(Paste)
  - Different than Mac Clipboard (⌘+c/x/v)
- **Search**
  - Search for a word named “Tyvek” in forward direction:
  - Press ESC key
  - Type /Tyvek
  - Hit n to search forwards for the next occurrence of word named “Tyvek”. You can press N to search backwards.
  - Search for a word named “bar” in backwards direction:
    - Press ESC key
    - Type ?bar
    - Hit N to search backwards for the next occurrence of word named “bar”. You can press n to search forwards.
  - Can you edit your .vimrc file and reload it without having to restart Vim?
  - reload current file: `:so %`
  - `%` stands for current file name
  - Re-load the currently active .vimrc: `:so $MYVIMRC`
- You can use wildcards with the :edit command. So, `:e **/test/Suite.java`
  - :e command should have tab complete
- to load a list of all files in the current directory into a buffer: `:r! find . -type f`
- Search for a word named “bar” in backwards direction:
  Press ESC key
  Type ?bar
  Hit N to search backwards for the next occurrence of word named “bar”. You can press n to search forwards.
- In normal mode, move the cursor to any word say 254.
  - Press * to search forwards for the next occurrence of word 254, or press # to search backwards:
- Search and open file from the CLI
  - The vi / vim text editor supports running any : command using the following syntax:
    - vi +commandHere fileName
    - vim +LineNumber fileName
    - vi +/searchTermHere fileName
    - vi +/LineNumberHere fileName
    - vim +/LineNumberHere fileName
  - To open file and go to function called main(), enter:
    - vim +/main filename-here
  - Next open file and go to line number 42, enter:
    - $ vim +42 fileName
  - [Open File And Go To Specific...](https://www.cyberciti.biz/faq/linux-unix-command-open-file-linenumber-function/)
  - (number) before key command: repeat commands (number) times
- **Replace**
  - For each line in [range] replace a match of {pattern} with {string}.
  - `:[range]s[substitute]/{pattern}/{string}/[c][e][g][p][r][i][I] [count]`
  - :s/search/replace/, it will search only the current line and match only the first occurrence of a term
  - Search – search forward type / and ? searches backwards; both followed immediately by the term to search for.
  - :%s/foo/bar will replace the first occurrence of foo with bar, operating on every line in the buffer.
  - :%s/foo/bar/g will replace every occurrence of foo with bar, operating on every line in the buffer.
  - :s/foo/bar will replace the first occurrence of foo with bar, operating on the current line.
  - :s/foo/bar/g will replace every occurrence of foo with bar, operating on the current line.
  - Also very helpful is the /c flag – it will allow you to confirm each replacement match, depending on the above criteria for searching.
    - %s/search/replace/gc.
  - \t = tab, \n = new line
  - % represents “global changes to all occurrences” replace to a line number, ending line number of comma.
    - :8,10 s/search/replace/g
  - Examples Search
    - `/word` Search word from top to bottom
    - `?word` Search word from bottom to top
    - `*` Search the word under cursor
    - `/string` Search STRING or string, case insensitive
    - `/jo[ha]n` Search john or joan
    - `/<` the Search the, theatre or then
    - `/the>` Search the or breathe
    - `/fred\|joe` Search fred or joe
    - `/\<\d\d\d\d\>` Search exactly 4 digits
    - `/^\n\{3}` Find 3 empty lines
    - `:bufdo /search str/` Search in all open files
    - `bufdo %s/something/` Search something in all the open buffers and
    - `something else/g` replace it with something else
  - Examples Replace
    - `:%s/old/new/g` Replace all occurrences of old by new in file
    - `:%s/onward/forward/gi` Replace onward by forward, case unsensitive
    - `:%s/old/new/gc` Replace all occurrences with confirmation
    - `:%s/^/hello/g` Replace the beginning of each line by hello
    - `:%s/$/Harry/g` Replace the end of each line by Harry
    - `:%s/onward/forward/gi` Replace onward by forward, case unsensitive
    - `:%s/ *$//g` Delete all white spaces
    - `:g/string/d` Delete all lines containing string
    - `:v/string/d` Delete all lines containing which didn’t contain string
    - `:s/Bill/Steve/` Replace the first occurrence of Bill by Steve in current line
    - `:s/Bill/Steve/g` Replace Bill by Steve in current line
    - `:%s/Bill/Steve/g` Replace Bill by Steve in all the file
    - `:%s/^M//g` Delete DOS carriage returns (^M)
    - `:%s/\r/\r/g` Transform DOS carriage returns in returns
    - `:%s#<[^>]\+>##g` Delete HTML tags but keeps text
    - `:%s/^\(.*\)\n\1$/\1/` Delete lines which appears twice
    - `Ctrl+a` Increment number under the cursor
    - `Ctrl+x` Decrement number under cursor
    - `ggVGg?` Change text to Rot13
- **Marks**
  - Use "M" followed by a character to set a mark
  - Marks A-Z,0-9: Jump to the mark in the file
    - Does not need to be open
  - Marks a-z: Jump to the mark in the current buffer.
  - Marks can be used as a motion
- **Split**
  - In Gvim and vim in terminals with mouse support, it is also possible to use the mouse to resize a window.
  - Simply grab the status line at the window border and drag it into the desired direction.
- **Spelling**
  - Turn Spelling on all: `:set spell spelllang=en_us`
  - Turn Spelling on local buffer only: `:setlocal spell spelllang=en_us`
  - Turn Spelling off: `set nospell`
  - Always on in vimrc: `set spell spelllang=en_us`
  - Turn on Automatically for .md files: `autocmd BufRead,BufNewFile *.md setlocal spell`
  - Set File for new words: `:set spellfile=~/.vim/spell/techspeak.utf-8.add`
    - :help spell-mkspell
    - Reload Spell: `:mkspell`
  - Turn on Word Completion (.vimrc): `set complete+=kspell`
    - P^ or N^ to bring completion
  - Spelling Colors: Highlight Term
    - SpellBad        word not recognized                     hl-SpellBad
    - SpellCap        word not capitalized                    hl-SpellCap
    - SpellRare       rare word                               hl-SpellRare
    - SpellLocal      wrong spelling for selected region      hl-SpellLocal

| Key     | Description              |
|---------|--------------------------|
| ]s      | next misspelled word     |
| ]S      | only bad words           |
| zg      | add word to spellfile    |
| zw      | add to bad word          |
| zuw/zug | undo add                 |
| z=      | suggest word             |
| [s      | previous misspelled word |
| [S      | previous bad words       |
| zG      | add to internal list     |
| zW      | add to internal list     |
| zuW/zuG | undo Add                 |
| zW      | add to internal list     |

- **Buffers**
- Flags
  - \- Inactive buffer
  - % Current buffer
  - \+ File has been modified
  - h Hidden buffer
  - \(num symbol) Alternate buffer
