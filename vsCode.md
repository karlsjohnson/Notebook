# VS Code

## Shortcuts

Look in vim Maps for a comparison

### Shortcuts-Cursor

| Shortcut   | Command              |
| :--------- | :------------------- |
| ⌥↑         | Move Line up         |
| ⌥⇧↑        | Copy Line up         |
| ⌥↓         | Move Line down       |
| ⌥⇧↓        | Copy Line down       |
| ⌘⇧K        | Delete Line          |
| ⌘Delete    | Delete all to Right  |
| ⌘Backspace | Delete all to Left   |
| ⌘Enter     | Insert Line Below    |
| ⌘⇧Enter    | Insert Line Above    |
| ^⇧J        | Join Line with Below |

### Shortcuts-Main

| Shortcut          | Command                         |
| :---------------- | :------------------------------ |
| ⌘K ⌘T             | Select Theme                    |
| ⌘K ⌘F             | Format Document                 |
| ⌘K ⌘F             | Show Keyboard Shortcuts         |
| ⌘K ⌘I             | Show Hover         |
| ⌘K V              | Preview Document to the side    |
| ⌘⇧P               | Command Palette                 |
| ⌥⌘B               | Toggle Sidebar                  |
| ⌘⇧O               | Goto Symbol in File             |
| ⌘K,V              | Open Preview                    |
| ⌃TAB              | Cycle Open Files                |
| ⌃⇧Z               | Toggle Word Wrap                |
| ⌃H or J or K or L | move cursor                     |
| ⌃⌥J or K          | page up,down                    |
| ⌘DEL              | Delete All to beginning of Line |
| ⌘FN,DEL           | Delete All to end of Line       |
| ^R| Workspace picker|

### Shortcuts-Sidebar

| Shortcut | Command       |
| :------- | :------------ |
| ⌘0       | Focus Sidebar |
| TAB      | Cycle Windows |
| ⌘⇧E      | Explorer Tab  |

**Navigation** Shortcuts

| Shortcut | Command                 |
| :------- | :---------------------- |
| ⌘1       | Focus First Editor      |
| ⌘2       | Focus Seconds Editor    |
| ⌘K ⌘➡    | Focus to Right          |
| ⌘K ⌘⬅    | Focus to Left           |
| ⌘K ⌘⬆    | Focus to Up             |
| ⌘K ⌘⬇    | Focus to Down           |
| ⌘^➡ or ⬅ | Move File Left or right |

**Folding** Shortcuts

| Shortcut | Command            |
| :------- | :----------------- |
| ⌥⌘[      | Fold               |
| ⌥⌘]      | Unfold             |
| ⌘K ⌘0    | Fold All           |
| ⌘K ⌘[    | Fold Recursively   |
| ⌘K ⌘]    | UnFold Recursively |
| ⌘K ⌘1    | Fold Level 1-7     |
| ⌘K ⌘J    | Unfold All         |
| ⌘K ⌘L    | Toggle Fold        |

## Configuration

### Config-Files

- Extension location: `~/.vscode`
- Settings file: `~/Library/Application Support/Code/User/settings.json`
- Shortcuts file: `~/Library/Application Support/Code/User/keybindings.json`:

### Config-Fonts

- American Typewriter
- Menlo
- "Note Mono"
- "Source Code Pro"
- "Courier New"
- Helvetica

## Plugins

### Markdown All in One

[Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)

| Shortcut            | Command                 |
| :------------------ | :---------------------- |
| ⌃⇧[ or ]            | Change Heading Level    |
| ⌘ [ or ]            | Indent / un-indent line |
| Select TAB or ⇧TAB  | Indent / un-indent line |
| ⌘B                  | Toggle Bold             |
| ⌘I                  | Toggle Italic           |
| ⌘K `                | Toggle Strikethrough    |
| Enter/Tab/Backspace | Create Lists            |
| CommandP            | Create TOC              |
| CommandP            | Update TOC              |

### Markdown Preview Enhanced

[Markdown Preview Enhanced](https://github.com/shd101wyy/vscode-markdown-preview-enhanced)

| Shortcut | Command                      |
| :------- | :--------------------------- |
| ⌘K V     | Preview Document to the side |
| ⌘⇧V      | Preview Document             |
| ⌃⇧S      | Sync Preview                 |

### Paste URL

[PasteURL](https://github.com/kukushi/PasteURL)

| Shortcut | Command            |
| :------- | :----------------- |
| ⌃⌥P      | Paste Markdown URL |

### Open File Under Cursor

[Open File](https://gitlab.com/fr43nk/seito-openfile)

| Shortcut | Command                |
| :------- | :--------------------- |
| ⌥O       | Open File Under Cursor |

### Text Tables

[Text Tables](https://github.com/rpeshkov/vscode-text-tables)

| Shortcut        | Command                   |
| :-------------- | :------------------------ |
| ^Q ^Q           | Enter Table Mode          |
| ^Q ^F           | Format Table Under Cursor |
| ^Q Space        | Clear Cell                |
| ⌥^TAB           | Next Cell                 |
| ⌥^⇧TAB          | Previous Cell             |
| Enter           | Next Row                  |
| Command Palette | Create table              |

### Table Formatter

[Markdown Table Formatter](https://github.com/fcrespo82/vscode-markdown-table-formatter)

### Code Spell Checker

[Code Spell Checker](https://github.com/streetsidesoftware/vscode-spell-checker)
[Marketplace-Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

| Shortcut | Command          |
| :------- | :--------------- |
| ⌘.       | Suggest Spelling |

Spelling Checker **Notes**

- Only words longer than 3 characters are checked. "jsj" is ok, while "jsja" is not.
- All symbols and punctuation are ignored.
- This spellchecker is case insensitive. It will not catch errors like english which should be English.
- The spellchecker uses a local word dictionary. It does not send anything outside your machine.
- The words in the dictionary can and do contain errors.
- There are missing words.

In Document **Settings**

- Disable Checking
  - `/* cSpell:disable */`
  - `/* spell-checker: disable */`
  - `/* spellchecker: disable */`
  - `/* cspell: disable-line */`
  - `/* cspell: disable-next-line */`
- (re)Enable Checking
  - `/* cSpell:enable */`
  - `/* spell-checker: enable */`
  - `/* spellchecker: enable */`
- Ignore allows you the specify a list of words you want to ignore within the document.
  - `// cSpell:ignore zaallano, wooorrdd`
  - `// cSpell:ignore zzooommmmmmmm`
  - `const wackyWord = ['zaallano', 'wooorrdd', 'zzooommmmmmmm'];`
- The words list allows you to add words that will be considered correct and will be used as suggestions.
  - `// cSpell:words woorxs sweeetbeat`
  - `const companyName = 'woorxs sweeetbeat';`
- Enable / Disable compound words
  - In some programing language it is common to glue words together.
  - `// cSpell:enableCompoundWords`
  - `char * errormessage;  // Is ok with cSpell:enableCompoundWords`
  - `int    errornumber;   // Is also ok.`
- Excluding and Including Text to be checked
  - Excluding and Including Text to be checked.
  - cSpell:disable/cSpell:enable above allows you to block off sections of the document.
  - ignoreRegExp and includeRegExp give you the ability to ignore or include patterns of text. By default the flags gim are added if no flags are given.
  - The spell checker works in the following way:
    - Find all text matching includeRegExp
    - Remove any text matching excludeRegExp
    - Check the remaining text.
    - Examples
    - ==Continue from Manual==
