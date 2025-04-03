# Vi/Vim Editor Cheat Sheet and Walkthrough 📜

A structured reference guide for efficient navigation and editing in Vi/Vim.

---

## Table of Contents 🔍
1. [What is Vi/Vim?](#what-is-vim-ℹ️)
2. [Modes of Operation](#modes-🕹️)
3. [Navigation](#navigation-🧭)
4. [Editing](#editing-✏️)
5. [Saving/Exiting](#savingexiting-💾)
6. [Search/Replace](#searchreplace-🔍)
7. [Advanced Features](#advanced-features-🚀)
8. [Quick Reference](#quick-reference-📋)
9. [Walkthrough](#walkthrough-🛠️)
10. [Tips](#tips-💡)
11. [Resources](#resources-📚)

---

<a name="what-is-vim-ℹ️"></a>
## 1. What is Vi/Vim? ℹ️
```text
- vi  : Original Unix text editor (1976)
- vim : Vi IMproved (modern enhanced version)
- Key Features:
  • Modal editing system
  • Lightweight & cross-platform
  • Extensible through .vimrc
  • Pre-installed on most Unix systems
<a name="modes-🕹️"></a>

2. Modes of Operation 🕹️
Mode	Entry Command	Description
Normal	Esc	Default mode for navigation
Insert	i, a, o	Text input mode
Visual	v	Character selection
Visual Line	V	Line selection
Visual Block	Ctrl+v	Block selection
Command-Line	:	Execute extended commands
<a name="navigation-🧭"></a>

3. Navigation 🧭
Basic Movement
vim
Copy
h    ← Left        l → Right
j    ↓ Down        k ↑ Up
w    Next word     b Previous word
0    Line start    $ Line end
gg   First line    G Last line
Screen Navigation
vim
Copy
Ctrl+f  Page down     Ctrl+b  Page up
H       Top screen    L       Bottom screen
zz      Center line   zt      Top-align line
<a name="editing-✏️"></a>

4. Editing ✏️
Text Manipulation
vim
Copy
i    Insert mode       a    Append mode
o    New line below    O    New line above
x    Delete char       dd   Delete line
dw   Delete word       D    Delete to line end
yy   Yank line         p    Paste after
u    Undo              Ctrl+r Redo
Advanced Editing
vim
Copy
ciw  Change inner word    ct"  Change till "
>>   Indent line          <<   Unindent line
.    Repeat last command  &    Repeat last substitution
<a name="savingexiting-💾"></a>

5. Saving/Exiting 💾
Command	Action
:w	Save file
:wq	Save and quit
:q!	Quit without saving
:x	Save and exit (if modified)
:saveas file	Save to new file
<a name="searchreplace-🔍"></a>

6. Search/Replace 🔍
Basic Search
vim
Copy
/pattern   Search forward
?pattern   Search backward
n          Next match
N          Previous match
Replacement
vim
Copy
:%s/old/new/g     Global replace
:%s/old/new/gc    Confirm each change
:10,20s/old/new   Replace lines 10-20
<a name="advanced-features-🚀"></a>

7. Advanced Features 🚀
Window Management
vim
Copy
:sp       Split horizontally    :vsp    Split vertically
Ctrl+ww   Cycle windows         Ctrl+wq Close window
Macros
vim
Copy
qa  Start recording macro 'a'
q   Stop recording
@a  Execute macro 'a'
Registers
vim
Copy
"ayy  Yank to register a
"ap   Paste from register a
:reg  View all registers
<a name="quick-reference-📋"></a>

8. Quick Reference 📋
text
Copy
┌─────────────┬──────────────────────────────┐
| Navigation  | h j k l  gg G  w b  / ? n N  |
| Editing     | i a o  x dd dw  yy p  u      |
| File Ops    | :w :q :e# :bn :bd            |
| Advanced    | qa @a  :sp :vsp  :%s//g      |
└─────────────┴──────────────────────────────┘
<a name="walkthrough-🛠️"></a>

9. Walkthrough 🛠️
Create File

bash
Copy
vim tutorial.txt
Insert Text

vim
Copy
i
Hello World
Press Esc
Save & Exit

vim
Copy
:wq
Reopen & Edit

vim
Copy
vim tutorial.txt
G  # Go to last line
o  # New line below
Add new content
:x  # Save and exit
<a name="tips-💡"></a>

10. Tips 💡
text
Copy
🔧 Configuration:
• :set number       Show line numbers
• :syntax on        Enable syntax highlighting
• :set mouse=a      Enable mouse support

🚨 Troubleshooting:
• Esc Esc         Force return to Normal mode
• :e!             Reload file (discard changes)
• vim -r file     Recover swap file
<a name="resources-📚"></a>

11. Resources 📚
text
Copy
1. Official Docs     → :help user-manual
2. Interactive Tutor → Run `vimtutor`
3. Online Practice   → https://www.openvim.com/
4. Cheat Sheet       → https://vim.rtorr.com/
5. Plugin Manager    → https://github.com/junegunn/vim-plug
Pro Tip: Create a ~/.vimrc with set nocompatible to enable modern features!
