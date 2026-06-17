# VIM Motion Shortcuts

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

## Copy/Paste

- 'y' to copy and 'p' to paste: by default it does these ops from the unnamed register, to do from a specific register, prefix these commands with "\<reg\>. e.g => prefix with "+ to do from system clipboard.
- 'yy' to copy a line, and 'p' then to paste it on the line below the cursor

## Modification

- 'ciw' for change in word.

## Selection

- 'yi\<bracket\>' to select all text between the brackets
- 'ya\<bracket\>' to select text including the brackets

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
