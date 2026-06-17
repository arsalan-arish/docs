# Vim Motion Shortcuts

## General

- 's' to delete a char and enter into insert mode
- 'f' key with the letter that you want to jump to in the current line.
- '$' key to jump to the end of line
- '0' key to jump to the start of line
- '(' and ')' keys to jump up and down the file, '{' and '}' to jump faster
- 'gg' to move to the start line
- 'G' to move to the last line
- 'w' to move to the start of the next word
- 'b' to move to the start of the previous word
- 'e' to move to the end of the next word
- 'a' to append
- 'i' to insert
- 'A' to append at the end of line
- 'I' to insert at the start of line
- 'o' to insert one line below
- 'O' to insert one line above
- '.' to repeat an operation on a word.
- 'u' to undo and ''ctrl+r' to redo. 'U' to undo the line
- '%' to jump between the starting and ending brackets, if the cursor is on either

## Copy/Paste

- 'y' to copy and 'p' to paste: by default it does these ops from the unnamed register, to do from a specific register, prefix these commands with "\<reg\>. e.g => prefix with "+ to do from system clipboard.
- 'yy' to copy a line, and 'p' then to paste it on the line below the cursor
- 'yiw' to copy the word under cursor

## Modification

- 'ciw' for change in word.
- 'j' to join the current and the next line.  
Alternatively, select the lines and press 'j' to join them
- '~' to toggle the case of the letter (upper and lower).  
'gUw' to upper the word  
'guw' to lower the word
'gUU' to uppet the line
'guu' to lower the line
- 'Ctrl+A' to increment the number under the cursor and 'Ctrl+Z' to decrement.

## Selection

- 'v' for visual mode and 'Ctrl+v' for Visual block mode
- Press 'I' or 'A' to insert or append in visual block mode
- 'yi\<bracket\>' to select all text between the brackets
- 'ya\<bracket\>' to select text including the brackets
- 'gv' to reselect the last selection

## Deletion

- 'dd' to delete a line
- 'dw' to delete the word. 'diw' to delete and also enter insert mode. 'dt\<char\>' to delete upto the char

## Search

- '/' to search forward  
'?' to search backwards.  
Enter to jump the first occurence.
- 'n' to iterate over search results  
'N' to iterate backwards.
- '*' to search for the current word forward,  
'#' to search for the current word backward

## Cursor jumping

- '``' to jump to the last cursor position
- '`.' to jump to the last edit
- 'm\<char\>' to bookmark the line with the specific character.  
then '`\<char\>' to jump the the bookmark location

## Folding

- zM: Closes (folds) all code blocks in the file.  
- zR: Opens (unfolds) all code blocks in the file.  
- za: Toggles a single code block open or closed at your cursor.

## Text Wrapping  

- :set wrap
- :set nowrap
- :set linebreak

## Numbering

- :set number
- :set relativenumber

## Indenting

- '==' to indent a line automatically  
Select lines and '=' to indent them automatically. '.' to repeat
- '>>' to indent 2 spaces forward and '<<' to indent 2 spaces backward.  
Select lines and '>' or '<' to indent specifically. '.' to repeat

## Macro Recording

- 'q' and letter to start recording keypresses into the buffer with that letter. Press 'q' again to stop it.
- '@' and letter to apply that macro recorded keys in the letter buffer from the current cursor position

## Extras

- ':sort' to semantically sort the file.  
':sort!' to sort reversed
- ':read \<path\>' to read an external file and write it on the cursor pos
- ':read !\<cmd\> to read from the stdout of an external CLI command
- ':jq .\<keyName\>' to use json query and write the value of the key in the cursor pos
- ':s/\<pattern\>/\<replacement\>' to change occurence of a pattern, s stands for substitute  
Add '/g' in the end to replace all occurences in the current line  
Add '/d' in the end to delete the pattern  
- ':g/\<pattern\>/\<replacement\>' to do the same to the whole file
- ':v/\<pattern\>/\<replacement\>' to delete the lines NOT matching the pattern
- ':reg' to view all the registers
- 'gx' to open the link under the cursor in browser
- 'gf' to open the filepath under the cursor in a new tab
- ':\<lineNumber\> to jump to the line

## NeoVim

- 'mksession \<filename\>' to save the whole IDE instance state
- 'source \<filename\>' to load that session back
