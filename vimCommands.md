# Vim Commands

- Shortcuts **keys**
  - (mot)=motion, either arrow keys or HJKL keys
  - (f)=a file name
  - (i)=a number
  - (n)=a name
  - (c)=a character
  - (cmd)= a command
  - (SRC)= added to vimrc (custom)
  - (add)= shortcut add to vimrc, not default
  - `%` stands for current file name
- (?)= need to do more research more
- (number) before key command: repeat commands (number) times

## Default Subject Map

### Default Cursor movement

| Description                                                       | Key       |
| ----------------------------------------------------------------- | --------- |
| move cursor left                                                  | h,j,k,l         |
| move to top of screen                                             | H         |
| move to middle of screen                                          | M         |
| move to bottom of screen                                          | L         |
| jump forwards to the start of a word                              | w         |
| jump forwards to the start of a word (contain punctuation)        | W         |
| jump forwards to the end of a word                                | e         |
| jump forwards to the end of a word (contain punctuation)          | E         |
| jump backwards to the start of a word                             | b         |
| jump backwards to the start of a word (contain punctuation)       | B         |
| move to matching character*                                       | %         |
| jump to the start of the line                                     | 0         |
| jump to the first non-blank character of the line                 | ^         |
| jump to the end of the line                                       | $         |
| jump to the last non-blank character of the line                  | g_        |
| go to the first line of the document                              | gg        |
| go to the last line of the document                               | G         |
| go to line 5                                                      | 5gg or 5G |
| jump to next occurrence of character x                            | fx        |
| jump to before next occurrence of character x                     | tx        |
| jump to previous occurrence of character x                         | Fx        |
| jump to after previous occurrence of character x                   | Tx        |
| repeat previous f, t, F or T movement                             | ;         |
| repeat previous f, t, F or T movement, backwards                  | ,         |
| jump to next paragraph (or function/block, when editing code)     | }         |
| jump to previous paragraph (or function/block, when editing code) | {         |
| center cursor on screen                                           | zz        |
| move screen down one line (without moving cursor)                 | Ctrl + e  |
| move screen up one line (without moving cursor)                   | Ctrl + y  |
| move back one full screen                                         | Ctrl + b  |
| move forward one full screen                                      | Ctrl + f  |
| move forward 1/2 a screen                                         | Ctrl + d  |
| move back 1/2 a screen                                            | Ctrl + u  |

> \* (default supported pairs: '()', '{}', '[]' - use :h match pairs in vim for more info)

### Default Normal

(mot)=motion, either arrow keys or HJKL keys

| Key      | Type     | Description                         |
| -------- | -------- | ----------------------------------- |
| A        | Normal   | Append after cursor                 |
| AS       | Normal   | Append end of line                  |
| I        | Normal   | Insert before cursor                |
| IS       | Normal   | Insert start of line                |
| O        | Normal   | Insert new line below               |
| OS       | Normal   | Insert new line above               |
| V        | Normal   | Enter Visual Mode                   |
| C        | Normal   | Enter Copy Mode                     |
| :        | Normal   | Enter CLI Command                   |
| ZS ZS    | Normal   | Save and Quit                       |
| ZS QS    | Normal   | Quit without Saving                 |
| U        | Normal   | Undo                                |
| US       | Normal   | Undo All                            |
| R^       | Normal   | Redo                                |
| G F      | N-Goto   | Goto file under cursor              |
| H        | N-Move   | Move Left                           |
| J        | N-Move   | Move Down                           |
| K        | N-Move   | Move Up                             |
| L        | N-Move   | Move Right                          |
| W        | N-Move   | jump by start of words(punctuation) |
| WS       | N-Move   | jump by words(space)                |
| E        | N-Move   | jump by end of words (punctuation)  |
| ES       | N-Move   | jump by end of words (spaces)       |
| B        | N-Move   | back by token                       |
| BS       | N-Move   | back by word                        |
| 0        | N-Move   | Jump to first column                |
| 6S       | N-Move   | first character (same as 0w)        |
| 4S       | N-Move   | end of line                         |
| MS       | N-Move   | Move to the middle of page          |
| U^       | N-Move   | Page Up (moves by half)             |
| D^       | N-Move   | Page Down                           |
| G G      | N-Move   | Go to Top                           |
| GS       | N-Move   | Go to Bottom                        |
| ]S       | N-Move   | forward by paragraph                |
| [S       | N-Move   | backward by paragraph               |
| (i)G     | N-Move   | Jump to Line i                      |
| HS       | N-Move   | Move to the top of page             |
| LS       | N-Move   | Move to the bottom of page          |
| 3S       | N-Move   | Find previous token (under cursor)  |
| 8S       | N-Move   | Find next token (under cursor)      |
| G T      | N-Window | Tab Next                            |
| G TS     | N-Window | Tab Previous                        |
| W^ Q     | N-Window | Window Close                        |
| W^ W     | N-Window | Window Switch Last                  |
| W^ (mot) | N-Window | Window Switch Motion                |
| W^ N     | N-Window | Window Split and New File           |
| W^ R     | N-Window | Window Rotate Position              |

### Default Visual

| Key            | Description                       |
| -------------- | --------------------------------- |
| v              | Visual mode, highlight characters |
| {Visual}x or d | Delete highlight                  |
| {Visual}X or D | Delete the highlighted lines      |
| V              | Visual mode, start high lines |
| {Visual}CTRL-H | Delete highlight(in Select mode)  |
| D              | Visual: Delete highlight          |
| DS             | Visual: Delete highlight line(s)  |
| Key            | Description                       |

### Default Insert

| Key        | Description                                            |
| ---------- | ------------------------------------------------------ |
| T^         | Insert Indent                                          |
| D^         | Remove Indent                                          |
| 0 D^       | Remove All Indent                                      |
| C-w      | Delete word before cursor                              |
| C-t      | Indent current line with by one shift width             |
| C-d      | Unindent current line with by one shift width           |
| C-f      | Move cursor to auto indent position                    |
| C-a      | Insert previously inserted text                        |
| C-e      | Insert the character below                             |
| C-h      | Delete one character backward                          |
| C-y      | Insert the character above                             |
| C-r(reg) | Insert the content of {register}                       |
| C-o{cmd} | execute normal command(cmd) without leaving mode       |
| C-n      | Next autocomplete option for the current word          |
| C-p      | Previous autocomplete option for the current word      |
| C-v      | Insert a character by its ASCII value in decimal       |
| C-v x     | Insert a character by its ASCII value in hexadecimal   |
| C-v u     | Insert a character by its unicode value in hexadecimal |
| C-k      | Enter a digraph                                        |

### Default CLI

| Key                   | Description                                |
| --------------------- | ------------------------------------------ |
| !                     | Enter CLI Command                          |
| cd                    | Change working directory                   |
| pwd                   | List working directory                     |
| save (f)              | Saves files as filename                    |
| e (f)                 | Edit file                                  |
| e                     | revert to saved file                       |
| e!                    | Revert (force discard)                     |
| e! (f)                | Edit file always                           |
| r (f)                 | Insert file below                          |
| r !(cmd)              | Execute (cmd) insert below                 |
| q                     | Quit                                       |
| q!                    | Quit without saving                        |
| qa                    | Quit all                                   |
| cq                    | Quit always                                |
| w file                | Save file                                  |
| wq                    | Save and quit                              |
| x                     | Save and quit                              |
| m (n)                 | move line to line (n)                      |
| m +-(n)               | move line up/down +-(n) lines              |
| 5,7m 21               | move lines 5, 6 and 7 to after line 21     |
| 5,7m 0                | move lines 5, 6 and 7 to before first line |
| 5,7m $                | move lines 5, 6 and 7 to after last line   |
| .,.+4m 21             | move 5 lines at current line to line 21    |
| (i)                   | N-MoveJump to Line i                       |
| shell                 | Open (CLI)                                 |
| marks                 | List all Marks                             |
| marks aB              | list marks a, B                            |
| delmarks a            | delete mark a                              |
| delmarks a-d          | delete marks a, b, c, d                    |
| so $MYVIMRC           | Reload .vimrc                              |
| so %                  | reload current file                        |
| r! find . -type f     | load list of current dir into buffer       |
| highlight             | Show highlighted terms                     |
| delmarks abxy         | delete marks a, b, x, y                    |
| delmarks!             | delete all lowercase marks                 |
| tabnew                | Tab New                                    |
| tabc                  | Tab Close                                  |
| tabmove (i)           | Tab move to postion (i)                    |
| split (f)             | Open file in second window                 |
| split (:sp)           | Split Window Split Horizontally            |
| vsplit (:vs)          | Split Window Split Vertically              |
| (i) Split file        | Opens a new window n lines high            |
| sp (f)                | Split horizontally, open file              |
| vs (f)                | Split vertically, open file                |
| resize 60             | Change split height to 60 rows             |
| res +5                | Change split height by 5                   |
| vertical resize 80    | Change split width to 80                   |
| vertical resize +5    | Change split width by 5                    |
| new                   | Open a new window horizontally             |
| vnew                  | Open a new window vertically               |
| buffers               | List buffers                               |
| ls                    | List buffers                               |
| b (n)                 | Goto buffer (n)                            |
| sb (n)                | Splits window and edit buffer              |
| :vertical sbuffer (n) | Splits vertically and edit                 |
| bn                    | Buffer Next                                |
| bp                    | Buffer Previous                            |
| bd                    | Delete the current buffer                  |
| bd!                   | Delete current buffer (forced))            |
| hide                  | close current window                       |
| only                  | keep only this window open                 |
| set filetype?         | Display file type                          |
| {i}gt                 | go to tab in position i                    |
| tabn                  | go to next tab                             |
| tabp                  | go to previous tab                         |
| tabfirst              | go to first tab                            |
| tablast               | go to last tab                             |
| tabnew                | Tab New                                    |
| tabc                  | Tab Close                                  |
| tabmove (i)           | Tab move to postion (i)                    |
| tabm 0                | move current tab to first                  |
| tabm                  | move current tab to last                   |
| tabm {i}              | move current tab to position i+1           |
| mks! (f)              | Save Current session to (F)                |
| so (f)                | Load session from (f)                      |

Now to open a new split and open the bar file inside it: `:sp bar`
To split the current split again, only vertically (and at the same time open the file named “dog”) run: `:vsp dog`
The size of the current split can be adjusted by using `Ctrl-w +` and `Ctl-w -`
For example to increase our current split (which is the cat split) by 5 lines run the following: `Ctrl-w 5+`
To quickly “maximize” the current split: `Ctrl-w _`
And to return to equalized splits: `Ctrl-w =`
|:sp filename |Open filename in horizontal split|
|:vsp filename |Open filename in vertical split|
|Ctrl-w h Ctrl-w ← |Shift focus to split on left of current|
|Ctrl-w l Ctrl-w → |Shift focus to split on right of current|
|Ctrl-w j Ctrl-w ↓ |Shift focus to split below the current|
|Ctrl-w k Ctrl-w ↑ |Shift focus to split above the current|
|Ctrl-w n+ |Increase size of current split by n lines|
|Ctrl-w n- |Decrease size of current split by n lines|

### Default Copy Paste

**Command** Mode **Yank, Delete, and Put**

Yank(Copy), Delete(Cut) and Put(Paste)
Different than Mac Clipboard (⌘+c/x/v)

| Key        | Description                               | Key      | Description              |
| ---------- | ----------------------------------------- | -------- | ------------------------ |
| (i)yy / :y | Copy line(s)                              |          |                          |
| (i)yW      | Copy word(s)                              | (i)yw    | Copy token(s)            |
| p          | Paste before cursor                       | P        | Paste after cursor       |
| (i)x       | Cut under/after cursor                    | (i)X     | Cut before cursor        |
| (i)dd      | Cut i lines                               | :d       | Cut i lines              |
| dw         | delete word                               | dl       | delete character         |
| D          | Cut under and to end of the line          | (i)s     | Cut at cursor and insert |
| dt(char)   | Cut to (not including) (char) on line     | df(char) | (including)              |
| di(char)   | Cut text bounded by (char)                | da(char) | (and including)          |
| (i)cw      | Correct (delete insert) the token(s)      | (i)cW    | Correct the word(s)      |
| ct(char)   | Correct to (not including) (char) on line | cf(char) | (and including)          |
| ci(char)   | Correct bounded by (char)                 | ca(char) | (and including)          |
| cc         | Correct Line                              |          |                          |

### Default Buffers

| Key           | Description                   | Key                      | Description                     |
| ------------- | ----------------------------- | ------------------------ | ------------------------------- |
| :buffers      | list buffers                  | :b number                | Select buffer number            |
| :sb number    | Splits window and edit buffer | :vertical sbuffer number | Splits vertically and edit      |
| :bnext or :bn | Go to the next buffer         | :bdelete                 | Deletes a buffer without saving |
| - (Flags)     | Inactive buffer               | h                        | Hidden buffer                   |
| %             | Current buffer                | #                        | Alternate buffer                |
| +             | File has been modified        |                          |                                 |

### Default Spelling

Turn Spelling on `:setlocal spell spelllang=en_us`
Turn on Automatically: `autocmd BufRead,BufNewFile *.md setlocal spell`
Reload Spell: `:mkspell`
| Key     | Description           | Key     | Description              |
| ------- | --------------------- | ------- | ------------------------ |
| ]s      | next misspelled word  | [s      | previous misspelled word |
| ]S      | only bad words        | [S      | previous bad words       |
| zg      | add word to spellfile | zG      | add to internal list     |
| zw      | add to bad word       | zW      | add to internal list     |
| zuw/zug | undo add              | zuW/zuG | undo Add                 |
| z=      | suggest word          | zW      | add to internal list     |

Colors: **Highlight Terms**

- SpellBad        word not recognized                     hl-SpellBad
- SpellCap        word not capitalized                    hl-SpellCap
- SpellRare       rare word                               hl-SpellRare
- SpellLocal      wrong spelling for selected region      hl-SpellLocal

### Default Other

Reload .vimrc  `:so $MYVIMRC`
Show highlighted terms: `:highlight`
:e filename      - edit another file
:split filename  - split window and load another file
ctrl-w up arrow  - move cursor up a window
ctrl-w ctrl-w    - move cursor to another window (cycle)
ctrl-w_          - maximize current window
ctrl-w=          - make all equal size
10 ctrl-w+       - increase window size by 10 lines
:vsplit file     - vertical split
:sview file      - same as split, but readonly
:hide            - close current window
:only            - keep only this window open
:ls              - show current buffers
:b 2             - open buffer #2 in this window

Editing a **File**

:shell Opens command prompt
:W save File

- :e[dit] | Edit the current ﬁle. This is useful to re-edit the current ﬁle, when it has been changed outside of Vim.
- :e[dit]! | Edit the current ﬁle always. Discard any changes to the current buffer. This is useful if you want to start all over again.
- :e[dit] {ﬁle} | Edit {ﬁle}.
- :e[dit]! {ﬁle} | Edit {ﬁle} always. Discard any changes to the current buffer.
- gf | Edit the ﬁle whose name is under or after the cursor. Mnemonic: "goto ﬁle".
- :y Yank the current line
- :d Delete current line
- :shell Opens command prompt
- :e filename Open a new file ỏ

Inserting a **file**

- :r[ead] [name] | Insert the ﬁle [name] below the cursor.
- :r[ead] !{cmd} | Execute {cmd} and insert its standard output below the cursor.

## Default Key Map

| Key        | Description                             |
| :--------- | :-------------------------------------- |
| \` (c)     | Move to position of mark (c)            |
| ` .        | Move to last change in current buffer   |
| ` "        | Move to last exited current buffer      |
| ` same     | Move back to position where jumped from |
| ` 0        | Move to last file edited (exited Vim)   |
| ` 1        | like 0 but the previous file (also 2)   |
| `S (mot)   | Switch case (character)                 |
| 1S(!)      | -unknown-                               |
| 2S(@)      | -unknown-                               |
| 3S(numsym) | Find previous token (under cursor)      |
| 4S($)      | Move end of line                        |
| 5S(%)      | Move to matching character (),[],{}     |
| 6S(^)      | Move first character (same as 0w)       |
| 7S(&)      | -unknown-                               |
| 8S(*)      | Move Find next token (under cursor)     |
| 9S(()      | Move sentences backward                 |
| 0          | Move Jump to first column               |
| 0S())      | Move sentences forward                  |
| -          | Move up line first non-blank char       |
| -S(_)      | Repeat "-"                              |
| =S(+)      | Repeat "ENTER"                          |
| =          | -unknown-                               |
| BACKSPACE  | Move Left                               |
| DELETE     | Cut Char                                |
| HOME       | Repeat "0"                              |
| END        | Repeat "$"                              |
| PageUp     | Repeat "^B"                             |
| PageDown   | Repeat "^F"                             |
| TAB        | -unknown-                               |
| Q (c)      | Macro Record with name of character     |
| QS         | Enter CLI                               |
| W          | Move jump word start                    |
| WS         | Move jump word start (space only)       |
| W^ (mot)   | Window Switch Motion                    |
| W^ N       | Window Split and New File               |
| W^ Q       | Window Close                            |
| W^ R       | Window Rotate Position                  |
| W^ W       | Window Switch Last                      |
| W^ R       | Window Rotate Position                  |
| W^ W       | Window Switch Last                      |
| W^ FS      | Open File in a new window               |
| W^ G FS    | Open file in a new tab                  |
| W^ (n)+    | Window adjust split size down           |
| W^ (n)-    | Window adjust split size up             |
| W^ (n)<    | Window adjust split size left           |
| W^ (n)>    | Window adjust split size right          |
| W^ _       | Window maximize height split            |
| W^ Pipe    | Window maximize width split             |
| W^ =       | Window equalize split                   |
| W^ (mot)   | Window Shift focus (mot)                |
| E          | Move jump word end                      |
| ES         | Move jump word end (space only)         |
| E^         | Move screen down one line               |
| R          | Replace Character                       |
| RS         | Insert Replace Mode                     |
| R^         | Redo                                    |
| -T-        | ?Extra Key Menu?                        |
| T (c)      | Move before next (c) right              |
| TS (c)     | Move before next (c) left               |
| Y (mot)    | Yank (Vim Copy)                         |
| YS         | Yank Line                               |
| Y^         | Move screen up one line                 |
| (n)Y Y     | Yank Line                               |
| (n)Y WS    | Yank word(s)                            |
| Y 4S       | Yank to end of line                     |
| (n)Y W     | Copy token(s)                           |
| U          | Undo                                    |
| US         | Undo All                                |
| U^         | Move half page up                       |
| I          | Insert before cursor                    |
| IS         | Insert start of line                    |
| OS         | Insert new line above                   |
| O          | Insert new line below                   |
| P          | Put (Paste) After                       |
| PS         | Put (Paste) Before                      |
| [          | Move sections forward                   |
| [ '        | Move previous line to mark              |
| [ `        | Move previous to lowercase mark         |
| [S({)      | Move backward by paragraph              |
| ]          | Move sections backward                  |
| ] '        | Move next line to mark                  |
| ] `        | Move next to mark                       |
| ]S(})      | Move forward by paragraph               |
| ]S         | Move forward by paragraph               |
| \          | Leader Key                              |
| \S         | -Unknown-                               |
| A          | Append after cursor                     |
| AS         | Append end of line                      |
| S          | Delete character, substitute text       |
| SS         | Delete line, substitute text            |
| -D-        | Extra Key - Delete                      |
| D(mot)     | Delete(cut) to (motion)                 |
| DS         | Delete(cut) to end of line              |
| D 4S       | Delete(cut) to end of line              |
| D D        | Delete(cut) line                        |
| D W        | Delete(cut) word                        |
| D^         | Move half page down                     |
| D T (c)    | Cut to not including (c) on line        |
| D F (c)    | Cut to including (c) on line            |
| D I (c)    | Cut text bounded by (c)                 |
| D I (c)    | Cut text (including) bounded (c)        |
| -F-        | ?Extra Key Menu?                        |
| F (c)      | Move onto next (c) right                |
| FS (c)     | Move onto next (c) left                 |
| F^         | Move page down                          |
| -G-        | Extra Key - Goto                        |
| GS         | Move Go to Bottom                       |
| (n)GS      | Move to line (n)                        |
| G -S(_)    | Move to last character of line          |
| G G        | Move Go to Top                          |
| (n) G G    | Move Go to line (n)                     |
| (n)G G     | Move to line (n)                        |
| G F        | Goto file under cursor (Same Window)    |
| G T        | Tab Next                                |
| G TS       | Tab Previous                            |
| G NS       | Tab New (SRC)                           |
| H          | Move Move Left                          |
| HS         | Move Move to the top of page            |
| J          | Move Move Down                          |
| JS         | Move Join Lines                         |
| K          | Move Move Up                            |
| KS         | -Unknown->Man Page?                     |
| L          | Move Move Right                         |
| LS         | Move Move to the bottom of page         |
| ;          | Repeat f,tF,T Forward                   |
| ;S         | Enter CLI Command                       |
| ' (c)      | Move to line of mark (c)                |
| ' '        | Move back to line where jumped from     |
| ' [        | Move to start of previously  text       |
| ' ]        | Move to end of previously  text         |
| ' ,S       | Move to start of last visual selection  |
| ' >        | Move to end of last visual selection    |
| 'S         | -Unknown-                               |
| ENTER      | Move down line first non-blank char     |
| -Z-        | Extra Key                               |
| Z .        | Center screen on cursor                 |
| Z Z        | Center screen on cursor                 |
| Z T        | Scroll screen so cursor at top          |
| Z B        | Scroll screen so cursor at bottom       |
| ZS QS      | Quit without Saving                     |
| ZS ZS      | Save and Quit                           |
| X          | Delete (cut) character forward          |
| XS         | Delete (cut) character backward         |
| X P        | transpose two letters                   |
| C (mot)    | Change (replace) to (motion)            |
| C I W      | Change (replace) entire word            |
| C W        | Change (replace) to end of word         |
| C WS       | Correct the word(s)                     |
| C 4S       | Change (replace) to end of line         |
| C          | Enter Copy Mode                         |
| CS         | change (replace) to end of line         |
| C C        | change (replace) entire line            |
| C T (c)    | Correct (not including) (c) on line     |
| C F (c)    | Correct (including) (c) on line         |
| C I (c)    | Correct bounded by (c)                  |
| C A (c)    | Correct bounded (including) by (c)      |
| V          | Enter Visual Mode                       |
| VS         | Enter Visual Mode (linewise)            |
| B          | Move back by token                      |
| BS         | Move back by word                       |
| B^         | Move page up                            |
| N          | Find Next from Search                   |
| NS         | Find Previous from Search               |
| M (c)      | Set Mark (c)                            |
| MS         | Move Move to the middle of page         |
| ,          | Repeat f,tF,T Backward                  |
| < (mot)    | Un-indent                               |
| .          | Repeat Command                          |
| > (mot)    | Indent                                  |
| /          | Find After                              |
| ?          | Find Before                             |

### Default Kep Map Unused

- What about ESC and Space?
- Tab for completions

| Key                  | Mode         | Type    | Notes                                                                                                                                                                                                                                                |
| -------------------- | ------------ | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Function keys        | All modes    | Free    | For instance, F6.                                                                                                                                                                                                                                  |
| Alt key combinations | All modes    | Free    | For instance, M-q. Note that mapping alt keys can be problematic depending on the terminal emulator. See e.g. :help :map-alt-keys for more information.                                                                                            |
| C-Q                | All modes    | Synonym | Synonym for C-V. This key is used for flow control on the terminal. On modern machines most people have no use for flow control so you can run stty -ixon in your shell to unlock it for your own use.                                             |
| C-S                | All modes    | Free    | Used for flow control like C-Q.                                                                                                                                                                                                                    |
| C-@                | Normal       | Free    | This can also be entered with C-Space.                                                                                                                                                                                                             |
| C-H                | Normal       | Synonym | Synonym for h.                                                                                                                                                                                                                                       |
| C-J                | Normal       | Synonym | Synonym for j.                                                                                                                                                                                                                                       |
| C-K                | Normal       | Free    |                                                                                                                                                                                                                                                      |
| C-N                | Normal       | Synonym | Synonym for j.                                                                                                                                                                                                                                       |
| C-P                | Normal       | Synonym | Synonym for k.                                                                                                                                                                                                                                       |
| C-[                | Normal       | Free    | This can also be typed as Esc.                                                                                                                                                                                                                     |
| C-_                | Normal       | Free    | This can also be typed as C-/.                                                                                                                                                                                                                     |
| +                    | Normal       | Synonym | Synonym for CR.                                                                                                                                                                                                                                    |
| K                    | Normal       |         | By default, this is an inferior version of Leader-K that can be obtained through man.vim with runtime! ftplugin/man.vim. See :help find-manpage for more.                                                                                           |
| S                    | Normal       | Synonym | Synonym for cc.                                                                                                                                                                                                                                      |
| Y                    | Normal       | Synonym | Synonym for yy. However, many people like to map this to y$ to match the behavior of C and D.                                                                                                                                                        |
| _                    | Normal       |         | This is nearly the same as CR. The documentation (:help maplocalleader) even mentions the underscore as an example of a key that can be used for the local leader.                                                                                 |
| s                    | Normal       | Synonym | Synonym for cl.                                                                                                                                                                                                                                      |
| x                    | Normal       | Synonym | Synonym for dl. However, it is handy to be able to repeat x several times in a row, whereas repeating dl gets cumbersome. (A similar problem does not exist for s and cl, since there is no point in repeating it.)                                  |
| Del                | Normal       | Synonym | Synonym for x.                                                                                                                                                                                                                                       |
| C-@                | Visual       | Free    | This can also be entered with C-Space.                                                                                                                                                                                                             |
| C-H                | Visual       | Synonym | Synonym for h (or BS in select mode).                                                                                                                                                                                                              |
| C-I                | Visual       | Free    | This is the Tab key, which does nothing in visual mode.                                                                                                                                                                                            |
| C-J                | Visual       | Synonym | Synonym for j.                                                                                                                                                                                                                                       |
| C-K                | Visual       | Free    |                                                                                                                                                                                                                                                      |
| C-N                | Visual       | Synonym | Synonym for j.                                                                                                                                                                                                                                       |
| C-O                | Visual       | Free    | In select mode, this switches to visual mode for one command. Mapping with xnoremap will map it only for visual mode while preserving the default behavior in select mode. See :help mapmode-x for more.                                             |
| C-P                | Visual       | Synonym | Synonym for k.                                                                                                                                                                                                                                       |
| C-R                | Visual       | Free    |                                                                                                                                                                                                                                                      |
| C-T                | Visual       | Free    |                                                                                                                                                                                                                                                      |
| C-^                | Visual       | Free    |                                                                                                                                                                                                                                                      |
| C-_                | Visual       | Free    | This can also be typed as C-/.                                                                                                                                                                                                                     |
| &                    | Visual       | Free    |                                                                                                                                                                                                                                                      |
| +                    | Visual       | Synonym | Synonym for CR.                                                                                                                                                                                                                                    |
| .                    | Visual       | Free    |                                                                                                                                                                                                                                                      |
| P                    | Visual       | Synonym | Synonym for p.                                                                                                                                                                                                                                       |
| Q                    | Visual       | Free    |                                                                                                                                                                                                                                                      |
| R                    | Visual       | Synonym | Synonym for S. However, the documentation (:help v_R) says "In a next version it might work differently."                                                                                                                                            |
| Z                    | Visual       | Free    | Z in visual mode waits for a following key, as seen if 'showcmd' is set. However, neither ZZ nor ZQ do anything (as in normal mode), and no other key combination is listed in the index, so it appears that Z actually does nothing in visual mode. |
| _                    | Visual       |         | Nearly the same as CR.                                                                                                                                                                                                                             |
| s                    | Visual       | Synonym | Synonym for c.                                                                                                                                                                                                                                       |
| x                    | Visual       | Synonym | Synonym for d.                                                                                                                                                                                                                                       |
| Del                | Visual       | Synonym | Synonym for d.                                                                                                                                                                                                                                       |
| C-B                | Insert       | Free    |                                                                                                                                                                                                                                                      |
| C-J                | Insert       | Synonym | Synonym for CR.                                                                                                                                                                                                                                    |
| C-Z                | Insert       | Free    | Unless 'insertmode' is set.                                                                                                                                                                                                                          |
| C-_                | Insert       | Free    | This can also be typed as C-/.                                                                                                                                                                                                                     |
| C-@                | Command-line | Free    | This can also be entered with C-Space.                                                                                                                                                                                                             |
| C-J                | Command-line | Synonym | Synonym for CR.                                                                                                                                                                                                                                    |
| C-O                | Command-line | Free    |                                                                                                                                                                                                                                                      |
| C-X                | Command-line | Free    |                                                                                                                                                                                                                                                      |
| C-Z                | Command-line | Free    |                                                                                                                                                                                                                                                      |
| C-_                | Command-line | Free    | This is only active in default Vim if 'allowrevins' is set, for right-to-left languages.                                                                                                                                                             |
