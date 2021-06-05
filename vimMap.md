# Vim

## New Shortcuts

- With Neovim Plugin, VSCode acts normal in insert mode

| Action                          | VimOrig  | NeoVim:N | Neovim:I | VSCode |
|---------------------------------|:--------:|:--------:|:--------:|:------:|
| Move Down/Up                    | j/k      | j/k      | ↓/↑      | ↓/↑    |
| Move Left/Right                 | h/l      | h/l      | ←/→      | ←/→    |
| Move Down/Up 1/2 Page           | ^d/\^u   | J/K      | -        | ^d/\^u |
| Move Down/Up Page               | ^f/\^b   | ^f/\^b   | -        | ^f/\^b |
| Move First/Last Character       | ^/$      | H/L      | ⌘←/⌘→    | ⌘←/⌘→  |
| Move Middle on Line             | gm       | M        | -        | -      |
| Move Next/Previous word (token) | w/b      | w/b      | ⌥→/⌥←    | ⌥→/⌥←  |
| Move Next/Prev word (no token)  | W/B      | W/B      | ⌥→/⌥←    | ⌥→/⌥←  |
| indent                          | << ^d    | ⌥,       | ⌥,       | ⌥,     |
| outdent                         | >> ^t    | ⌥.       | ⌥.       | ⌥.     |
| undo                            | u        | ⌥z       | ⌥z       | ⌥z     |
| redo                            | ^r       | ⌥Z       | ⌥Z       | ⌥Z     |
| Scroll Page Top/Bottom          | gg/G     | gg/G     | gg/G     | ⌘↑/⌘↓  |
| Scroll to Top/Bottom/Middle     | z t/b/.  | z t/b/.  |          |        |
| Move to On/Before(c))           | f/t (c)  | f/t (c)  |          |        |
| Repeat F/T (forward/reverse)    | ;/,      | ;/,      |          |        |
| Goto Function Start/Next        | [[//]]   | [[//]]   |          |        |
| Goto Block Start/End            | [{//}]   | [{//}]   |          |        |
| Move around Panes               | ^h/j/k/l | ^h/j/k/l |          |        |
| NerdTree Toggle                 |          | ⌥b       |          |        |
| NerdTree File                   |          | ⌥⇧b      |          |        |

## Vim Start

| Action                            | Key |
| --------------------------------- | --- |
| neovim                            | vi  |
| neovim at Text Folder             | vit |
| neovim at Git Folder              | vig |
| neovim open dotFiles readme (git) | vid |
| neovim open Thoughts readme (git) | vis |
| neovim session current            | vsc |
| neovim session dotFiles           | vsd |
| neovim session git                | vsg |

## Vim Move

| Action                       | Key      |
| ---------------------------- | -------- |
| Down/Up                      | j/k      |
| Left/Right                   | h/l      |
| Scroll Down/Up 1/2 Page      | J/K      |
| First/Last Character         | H/L      |
| Scroll Page Top/Bottom       | gg/G     |
| Scroll to Top/Bottom/Middle  | z t/b/.  |
| Move word start (token/word) | w/W      |
| Move word end (token/word)   | e/E      |
| Move back (token/word)       | b/B      |
| Move to On/Before(c))        | f/t (c)  |
| Repeat F/T (forward/reverse) | ;/,      |
| Goto Function Start/Next     | [[//]]   |
| Goto Block Start/End         | [{//}]   |
| Move around Panes            | ^h/j/k/l |

## Vim Mode

| Action                | Key |
| --------------------- | --- |
| Return to Normal      | ESC |
| --**Insert**--        | --  |
| Insert before cursor  | i   |
| Insert start of line  | I   |
| Insert new line below | o   |
| Insert new line above | O   |
| Append after cursor   | a   |
| Append end of line    | A   |
| Change end of line    | C   |
| Change line           | c c |
| Replace Character     | r   |
| Insert Replace Mode   | R   |
| --**Visual**--        | --  |
| Visual Mode           | v   |
| Select Block          | ^v  |
| Visual Line Mode      | V   |
| Yank                  | y   |
| Put                   | p   |
| Cut                   | d   |

## Vim View

| Action                  | Key      |
|-------------------------|----------|
| **Tabs**                |          |
| Delete Tab              | d T      |
| New Tab                 | g N      |
| Goto Tab 1-6            | g 1-6    |
| List                    | g b      |
| **Windows(Tmux Panes)** | -----    |
| Close Window            | ^w c     |
| Move Panes Down/Up      | J/K^     |
| New Vertical Window     | W^ V     |
| Win Switch Motion       | W^ (mot) |
| Win adjust size down    | W^ (n)+  |
| Win adjust size left    | W^ (n)<  |
| Win maximize height     | W^ _     |
| New Horizontal Win      | W^ S     |
| Win Switch Last         | W^ W     |
| Win adjust size up      | W^ (n)-  |
| Win adjust size right   | W^ (n)>  |
| Win maximize width      | W^ Pipe  |
| Win Rotate Position     | W^ R     |
| Win equalize split      | W^ =     |
| --**Buffers**--         | -----    |
| Next                    | TAB      |
| Previous                | ⇧TAB     |
| Delete                  | d b      |
| --**Sessions**--        | ------   |
| Save dot-files          | lr S S D |
| Save New                | lr S S N |
| Save Current            | lr S S C |
| Save Write              | lr S S W |
| Recall dot-files        | lr S R D |
| Recall New              | lr S R N |
| Recall Current          | lr S R C |
| Recall Write            | lr S R W |
| --**Format**--          | ------   |
| Word Wrap               | Z W      |
| Action                  | Key      |
| Format Table            | Lr M K   |

## Vim File

| Action                   | Key    |
| ------------------------ | ------ |
| --**Go**--               | ---    |
| Open File                | g o    |
| Open Link                | g x    |
| Open Markdown            | g e    |
| Open File Under Cursor   | g f    |
| --**Markdown**--         | ---    |
| Goto MD Headers          | g h    |
| Format Table             | lr m f |
| MD Table of Contents Hor | lr m t |
| MD Table of Contents Ver | lr m v |
| --**Open**--             | ---    |
| Open File Init           | lr f v |
| Open File Tasks          | lr f t |
| Open File ~/.myInit      | lr f i |
| Open File ~/.zshrc       | lr f z |
| Source Init              | lr s v |
| Open File Links          | lr f l |
| Open File act.sh         | lr f a |
| NerdTree Toggle          | ⌥b     |
| NerdTree File            | ⌥⇧b    |
| --**Files**--            | ---    |
| Save                     | z s    |
| Quit All                 | Z Z    |
| Save All                 | z S    |
| Save All  & Quit         | Z S    |
| --**Directories**--      | ---    |
| List Current Dir         | lr d l |
| Goto Dir Documents       | lr d d |
| Goto Dir Desktop         | lr d p |
| Goto Dir Root            | lr d r |
| Goto Dir Text            | lr d t |
| Goto Dir Downloads       | lr d w |
| Goto Dir Git             | lr d g |

## Vim Edit

| Action              | Key       |
| ------------------- | --------- |
| Undo All            | U         |
| Undo                | u         |
| Redo                | ^r        |
| --**Edit**--        | ------    |
| Yank Line           | y y       |
| Yank to End         | y $       |
| Yank (Copy)         | y(mot)    |
| Yank Word           | y W       |
| Put (Paste) After   | p         |
| Put Before          | P         |
| Delete(cut)         | d(mot)    |
| Cut Left            | Backspace |
| Del line            | d d       |
| Del to end of line  | D         |
| Correct End of Line | C         |
| Join Lines          | z j       |
| Cut                 | Delete    |

## vimFunctions

| Action                   | Key    |
| ------------------------ | ------ |
| --**Search**--           | ------ |
| Search Down              | /      |
| Next                     | n      |
| Done                     | Enter  |
| Search Word under cursor | *      |
| Search Up                | ?      |
| Previous                 | N      |
| Deselect                 | d s    |
| --**Macros**--           | ------ |
| Start Macro (l)          | q (l)  |
| Execute macro (l)        | @ (l)  |
| Stop Macro               | q      |
| Execute Macro Again      | @@     |

## vimPlugins

| Action                | Key    |
| --------------------- | ------ |
| Goto #                | g h    |
| ToC Vertical          | lr m t |
| Goto Anything         | g a    |
| TableFormat           | lr m f |
| ToC Horizontal        | lr m t |
| --**Drawer**--        | ------ |
| Activate Drawer       | lr m d |
| Cut Header Contents   | D      |
| Goto Header           | o      |
| Paste Header Contents | p      |
| Increase Header       | -      |
| Decrease Header       | +      |

## vimCLI

| Action            | Key |
| ----------------- | --- |
| Enter CLI Command | !   |
| Change Dir        | cd  |

## vimOpen Keys

| Action     | Key   |
| ---------- | ----- |
|            | M/sM/ |
|            | ^M    |
|            | X     |
|            | XS    |
|            | YS    |
|            | GS    |
| Menu Key   | G     |
| Menu Key   | Z     |
| Menu Key   | D     |
| Menu Key   | \     |
| Leader Key | Space |
