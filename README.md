Here's the complete, polished Vi/Vim cheat sheet in a single Markdown file with perfect GitHub formatting and section linking:

```markdown
# Vi/Vim Editor Master Cheat Sheet 🚀

_A comprehensive guide to Vim commands and workflows with GitHub-optimized formatting_

---

## Table of Contents
1. [What is Vi/Vim?](#what-is-vivim)
2. [Modes](#modes)
3. [Navigation](#navigation)
4. [Editing](#editing)
5. [Saving/Exiting](#savingexiting)
6. [Search/Replace](#searchreplace)
7. [Advanced Features](#advanced-features)
8. [Quick Reference](#quick-reference)
9. [Walkthrough](#walkthrough)
10. [Tips](#tips)
11. [Resources](#resources)

---

## What is Vi/Vim? <a name="what-is-vivim"></a>
```text
- vi  : Original Unix text editor (1976)
- vim : Modern "Vi IMproved" version
- Key Features:
  • Modal editing (Normal/Insert/Visual modes)
  • Lightweight & available on all Unix systems
  • Highly customizable via ~/.vimrc
  • Powerful keyboard-driven workflow
```

---

## Modes <a name="modes"></a>
| Mode          | Entry          | Description                  |
|---------------|----------------|------------------------------|
| **Normal**    | `Esc`          | Default command mode         |
| **Insert**    | `i`, `a`, `o`  | Text insertion               |
| **Visual**    | `v`            | Character selection          |
| Visual Line   | `V`            | Line selection               |
| Visual Block  | `Ctrl+v`       | Column block selection       |
| Command-Line  | `:`            | Execute Ex commands          |

---

## Navigation <a name="navigation"></a>
### Basic Movement
```vim
h    ← Left        l → Right
j    ↓ Down        k ↑ Up
0    Line start    $ Line end
gg   First line    G Last line
w    Next word     b Previous word
```

### Screen Navigation
```vim
Ctrl+f  Page down       Ctrl+b  Page up
H       Top of screen   L       Bottom screen
zt      Top-align line  zz      Center line
```

---

## Editing <a name="editing"></a>
### Text Manipulation
```vim
i    Insert before cursor    a    Append after cursor
o    New line below          O    New line above
x    Delete character        dd   Delete line
dw   Delete word             D    Delete to line end
yy   Yank (copy) line        p    Paste after cursor
```

### Advanced Editing
```vim
ciw  Change inner word    cis  Change inner sentence
>>   Indent line          <<   Unindent line
u    Undo                 Ctrl+r Redo
.    Repeat last command
```

---

## Saving/Exiting <a name="savingexiting"></a>
```vim
:w        " Save file
:q        " Quit
:wq       " Save and quit
:q!       " Force quit without saving
:w newfile " Save as new file
ZZ        " Save+exit (Normal mode)
```

---

## Search/Replace <a name="searchreplace"></a>
### Search Commands
```vim
/pattern   " Search forward
?pattern   " Search backward
n          " Next match
N          " Previous match
*          " Search word under cursor
```

### Replacement
```vim
:%s/old/new/g      " Replace all
:%s/old/new/gc     " Confirm changes
:10,20s/old/new/g  " Lines 10-20
```

---

## Advanced Features <a name="advanced-features"></a>
### Window Management
```vim
:split     " Horizontal split
:vsplit    " Vertical split
Ctrl+ww    " Cycle windows
Ctrl+wq    " Close window
```

### Macros
```vim
qa  " Start recording macro 'a'
q   " Stop recording
@a  " Execute macro 'a'
5@a " Repeat 5 times
```

### Registers
```vim
"ayy  " Yank to register a
"ap   " Paste from register a
:reg   " View all registers
```

---

## Quick Reference <a name="quick-reference"></a>
```text
┌──────────────┬───────────────────────────────┐
| Navigation   | h j k l  gg G  w b  / ? n N  |
| Editing      | i a o  x dd dw  yy p  u      |
| File Ops     | :w :q :e# :bn :bd            |
| Advanced     | qa @a  :sp :vsp  :%s//g      |
└──────────────┴───────────────────────────────┘
```

---

## Walkthrough <a name="walkthrough"></a>
1. **Create and edit file:**
   ```bash
   vim tutorial.txt
   ```
   ```vim
   i
   Line 1: Vim is powerful
   Line 2: Modal editing rocks
   Esc
   ```

2. **Edit content:**
   ```vim
   /powerful  " Find typo
   cwawesome  " Change word
   :%s/rocks/rule/g  " Replace text
   ```

3. **Save and exit:**
   ```vim
   :wq
   ```

---

## Tips <a name="tips"></a>
### Essential Configuration
```vim
" ~/.vimrc basics:
set number         " Show line numbers
syntax on          " Enable syntax highlighting
set mouse=a        " Allow mouse support
set incsearch      " Highlight matches while typing
```

### Troubleshooting
```text
💡 Stuck? Press Esc Esc 
💡 Recover file: vim -r filename
💡 Clear search highlight: :noh
💡 Reload file: :e!
```

---

## Resources <a name="resources"></a>
1. [Official Documentation](https://www.vim.org/docs.php)
2. Interactive Tutorial: Run `vimtutor` in terminal
3. [OpenVim Interactive Trainer](https://www.openvim.com/)
4. [Vim Adventures Game](https://vim-adventures.com/)
5. [Vim Cheat Sheet](https://vim.rtorr.com/)

---

> **Pro Tip:** Create practice file with `vimtutor practice.txt` and experiment freely!
```

