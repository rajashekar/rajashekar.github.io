<!--
.. title: VIM vs EMACS
.. slug: vim-vs-emacs
.. date: 2020-06-17 09:56:46 UTC-07:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

|                       VIM                         |                   EMACS                             |
|---------------------------------------------------|-----------------------------------------------------|
|---------------------------------------------------|-----------------------------------------------------|
|               **Navigation**                      |                   **Navigation**                    |       
| j - move one line down                            | C-n move one line down                              |
| k - move one line up                              | C-p move one line up                                |
| l - move cursor right                             | C-f move cursor right                               |
| h - move cursor left                              | C-n move cursor left                                |
| w - move cursor one word forward                  | M-f move cursor one word forward                    |
| b - move cursor one word backward                 | M-b move cursor one word backward                   |
|                                                   |                                                     |
| H moves cursor to HOME of the window              | M-0 M-r moves cursor to HOME of the window          |
| M moves cursor to MIDDLE of the window            | M-m M-r moves cursor to MIDDLE of the window        |
| L moves cursor to BOTTOM of the window            | M-- M-r moves cursor to BOTTOM of the window        |
|                                                   |                                                     |
| gg - go to beginning of the buffer                | M-< or ESC-< go to beginning of the buffer          |
| G - go to end of the buffer                       | M-> or ESC-> go to end of the buffer                |
|                                                   |                                                     |
<!-- TEASER_END -->
| 0 or ^ - go to start of line                      | C-a go to start of line                             |
| $ - go to end of line                             | C-e go to end of line                               |
|                                                   |                                                     |
| Ctrl-f to forward one page                        | C-v to forward one page                             |
| Ctrl-b to backward one page                       | M-v to backward one page                            |
|                                                   |                                                     |
| ESC - to kill current command                     | C-g to kill current command                         |
| n <cmd> to repeat command n times                 | M-n <cmd> to repeat command n times                 |
|                                                   |                                                     |
| :set number to show line numbers                  | M-x global-linum-mode                               |
| To load by default (:set number) in .vimrc        | To load by default (global-linum-mode 1) in .emacs  |
|                                                   |                                                     |
| Wrap lines                                        |                                                     |
| :set nowrap - to remove wrapping of lines         | Wrap lines                                          |
| :set wrap - to enable wrapping of lines           | M-x toggle-truncate-lines                           |
|                                                   | (setq-default truncate-lines t)                     |
| :shell or sh go to shell                          | M-x shell go to shell                               |
| exit to come back to vi                           | Use C-x right or left to go next or previous buffer |
|                                                   |                                                     |
| :n to jump to line n                              | M-g g n to go to line n                             |
|                                                   |                                                     |
|                                                   | C-M-f find matching parenthesis forward             |
| % find matching parenthesis                       | C-M-b find matching parenthesis backward            |
|                                                   |                                                     |
|                                                   | M-/ for word completion                             |
| (insert mode)Ctrl+p or Ctrl+n for word completion |                                                     |
|                                                   | M-x sort-lines to sort                              |
| :sort to sort                                     |                                                     |
|                                                   | M-x line-number-mode                                |
| :set textwidth=190                                | M-x column-number-mode                              |
| (come to next line once 190 column is reached)    | C-x f to set column width                           |
|                                                   | M-q to wrap the current paragraph with column width |
|---------------------------------------------------|-----------------------------------------------------|
| **Undo**                                          |  **Undo**                                           |
| u - undo                                          | C-_ or C-x u or C-z to undo                         |
|---------------------------------------------------|-----------------------------------------------------|
| **Search**                                        |  **Search**                                         | 
| :set incsearch to set increment search            | By default increment search                         |
| :set ignorecase to set ignore case while search   | By default ignore case while search                 |
|                                                   |                                                     |
| /word to search forward                           | C-s to search forward                               |
| n- go to next match                               | C-s go to next match                                |
| N- go to previous match                           | C-r go to previous match                            |
|                                                   |                                                     |
| ?word to search backward                          | C-r to search backward                              |
| n- go to next match                               | C-r go to next match                                |
| N- go to previous match                           | C-s go to previous match                            |
|                                                   |                                                     |
| By default regexp search                          | Use C-M-s or C-M-r for regexp search.               |
|                                                   | or Esc-C-r or Esc-C-s                               |
| * or gd - to search word under cursor forward     |                                                     |
| # - to search word under cursor backward          | C-s C-w to search word under cursor forward         |
|                                                   | C-r C-w to search word under cursor backward        |
|                                                   | C-s C-M-y to start searching the selection          |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Column editing**                                                          | **Column editing**                                                                            |
| Ctrl+q or Ctrl+v to start column editing                                    | M-x cua-mode to enable column editing (toggles)                                               |
| I <any-character> ESC - to start insert at start of the block               | C-RET to start the selection (toggles)                                                        |
| A <any-character> ESC - to start insert at end of the block                 | once mark is set traverse using C-n/p/f/b/a/e to select region                                |
| h/j/k/l to select the block.                                                | After selection                                                                               |
| d - cut the selected region                                                 | C-x to cut the selected region                                                                |
| y - yank the selected region                                                | C-c or M-w to copy the region                                                                 |
| gv - to select the previous visual selection.                               | C-y or C-v to paste the region                                                                |
|                                                                             | Start typing having mouse at the start of the                                                 |
|                                                                             | region to insert at the start of region                                                       |
|                                                                             | Same goes to end of the region                                                                |
|                                                                             | Ret to move around the corners of the region.                                                 |
|                                                                             |                                                                                               |
|                                                                             | Rectangles -                                                                                  |
|                                                                             | C-Space to set mark                                                                           |
|                                                                             | move to any other region,                                                                     |
|                                                                             | C-x r k to kill the region                                                                    |
|                                                                             | C-x r y to paste that region                                                                  |
|                                                                             | C-x r c to clear the region with spaces                                                       |
|                                                                             | C-x r t String to replace rectangle block with String                                         |
|                                                                             | C-x r r a to copy the rectangle area to register a                                            |
|                                                                             | C-x r i a to paste the rectangle area to register a                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Replace**                                                                 | **Replace**                                                                                   |
| :%s/xyz/abc/g  - to replace xyz with abc                                    | M-x replace-string RET xyz RET abc RET to replace xyz with abc                                |
| :%s/xyz/abc/gc - to replace xyz with abc with confirmation.                 | M-x query-replace RET xyz RET abc RET to replace xyz with abc                                 |
|                                                                             | by asking user                                                                                |
|                                                                             | <SPACE> to replace                                                                            |
|                                                                             | <DEL> to skip                                                                                 |
|                                                                             | ! to replace others                                                                           |
|                                                                             |                                                                                               |
|                                                                             | M-% to replace same as M-x query-replace                                                      |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Cut, Copy and Paste**                                                     | **Cut, Copy and Paste**                                                                       |
| 0D or ^D - cut from cursor to end of line (no newline)                      | C-k cut from current cursor to end of the line (no newline)                                   |
| dd or Vd - cut current cursor to end of line (including current line)       | C-k C-k to cut the whole line (including new line)                                            |
| D - cut from current cursor to end of line (no newline)                     | C-Shift-n C-w to cut the current line (including new line)                                    |
| x  - to delete character under cursor                                       | M-k cut from current cursor to end of sentence                                                |
| dw - delete next word                                                       | C-d to delete next character                                                                  |
| yy or Vy - to copy current line (including current line)                    | <Delete> to delete previous character                                                         |
| ddp - swap current line and next line                                       | M-d to delete next word                                                                       |
|                                                                             | M-<Delete> to delete previous words                                                           |
|                                                                             | C-y paste                                                                                     |
|                                                                             | C-@ or C-Space mark set                                                                       |
|                                                                             | C-w cut from mark set to cursor                                                               |
|                                                                             | M-w Copy from mark set to cursor                                                              |
|                                                                             | C-a C-Space C-n M-w to copy whole line  (including new line)                                  |
|                                                                             | C-Shift-n M-w to copy the whole line (including new line)                                     |
|                                                                             | C-a C-Space C-n C-w C-n C-y swap current line and next line                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Indenting XML**                                                           | **Indenting XML**                                                                             |
| :set ft=xml                                                                 | M-x nxml-mode                                                                                 |
| :%s/>\s*</>\r</g                                                            | M-x replace-regexp RET  > *< RET >C-q C-j< RET                                                |
| ggVG=                                                                       | C-M-\ to indent                                                                               |
| J - to join line with one space                                             | M-x replace-regexp RET C-q C-j RET Space RET join lines 1 space                               |
| gJ - to join lines with no space                                            | M-x replace-regexp RET C-q C-j RET RET to join lines no space                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Dealing with case**                                                       | **Dealing with case**                                                                         |
| gUU - to make whole current line to upper case                              | C-a C-Space C-n C-x C-u - to make whole current line to uppercase                             |
| guu - to make whole current line to lower case                              | C-a C-Space C-n C-x C-l - to make whole current line to lowercase                             |
| ggVGU - to make whole file to upper case                                    | M-< C-Space M-> C-x C-u - to make whole file to upper case                                    |
| ggVGu - to make whole file to lower case                                    | M-< C-Space M-> C-x C-l - to make whole file to lower case                                    |
| ~ - to invert case.                                                         | M-l to make next word lower case                                                              |
|                                                                             | M-u to make next word upper case                                                              |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Dealing with files & Buffers**                                            | **Dealing with files & Buffers**                                                              |
| :e filename/vi filename to open file in vi                                  | C-x C-f to find the file to load into buffer                                                  |
| :view filename to only view the file. restricted to write                   | C-x C-q to only view the file. restricted to write (toggles)                                  |
| :set ro readonly mode                                                       | C-x b *scratch* to edit new file                                                              |
| :set ro! readonly mode                                                      | C-x 2 to split horizontally same file                                                         |
| :enew to edit new file                                                      | C-x 3 to split vertically same file                                                           |
| :sp to edit same file in H split                                            | C-x 4 C-f *scratch* to open file in H split                                                   |
| :vsp to edit same file in V split                                           | C-x 4 b buffer to open buffer in V split                                                      |
| :new to edit new file in H split                                            | C-x 3 C-x b buffer to open new buffer in V split                                              |
| :vnew to edit new file in V split                                           | C-x C-s to save buffer to file                                                                |
| :tabe to edit new file in new tab                                           | C-x s to save some buffers                                                                    |
| :e! return to unmodified file                                               | C-c C-x to exit emacs                                                                         |
| :q to quit                                                                  | to maximize in vertical split                                                                 |
| :q! to quit without save                                                    |                                                                                               |
| :wq to save and quit                                                        |                                                                                               |
| :w to write and be there in program                                         | C-x C-b to list all buffers                                                                   |
| :x to write and exit                                                        | C-x <Right> go to next buffer                                                                 |
| :x! not to write and exit                                                   | C-x <Left> go to previous buffer                                                              |
| ZZ to save and exit in command mode (capital Z)                             | C-x k to kill current buffer                                                                  |
| :w filename to write the content on file                                    | C-x b <buffer name> to switch to that buffer                                                  |
| :w! filename2 to overwrite the existing filename to filename2               | C-x h select everything in buffer                                                             |
|                                                                             | M-x buffer-menu to list all buffers in separate window                                        |
| :ls to list all the buffers                                                 | ~ clear modified flag on that buffer                                                          |
| :buffers to list all buffers                                                | k mark buffer for delete                                                                      |
| :buffer n to jump to buffer n                                               | x to delete all marked buffers                                                                |
| :bp to move to previous buffer                                              | o to open the buffer in below split window                                                    |
| :bn to move to next buffer                                                  | Note - * says it is modified, % means it is read only file                                    |
| :bd to remove from buffer                                                   | C-x 1 keep open only the current window                                                       |
| :args **/* to keep all files in the current directory in vim (SUPER)        | M-x make-frame same as above                                                                  |
| :rew to first file in args                                                  | C-x o to switch between windows                                                               |
| :te Buffers to show the menu buffer                                         | C-M-v to scroll the other window                                                              |
| :badd add file to buffer                                                    |                                                                                               |
| :b# to alternate buffer                                                     | C-x } to increase the size of window horizontally                                             |
| Ctrl-^ is to switch alternate buffers                                       | C-x { to decrease the size of window vertically                                               |
| :tab ball to open all buffers in tabs                                       |                                                                                               |
| :ball to open all buffers Horizontally                                      |                                                                                               |
| :vert ball to open all buffers vertically                                   |                                                                                               |
|                                                                             |                                                                                               |
| ctrl+w o keep open only the current window                                  |                                                                                               |
| ctrl+w w to switch between windows                                          |                                                                                               |
| ctrl-w-v to open a new window vertically                                    |                                                                                               |
| ctrl-w-n to open a new window horizontally                                  |                                                                                               |
|                                                                             |                                                                                               |
| ctrl-w + increase the size of window                                        |                                                                                               |
| ctrl-w - decrease the size of window                                        |                                                                                               |
| ctrl-w = to equalize the size of each split window                          |                                                                                               |
| ctrl-w                                                                      |                                                                                               |
| ctrl-w _ to maximize in Horizontal split                                    |                                                                                               |
| ctrl-w h to move to the window left                                         |                                                                                               |
| ctrl-w j to move to the window below                                        |                                                                                               |
| ctrl-w k to move to the window above                                        |                                                                                               |
| ctrl-w l to move to the window right                                        |                                                                                               |
| ctrl-w H to move current window to far right                                |                                                                                               |
| ctrl-w J to move current window to far Down                                 |                                                                                               |
| ctrl-w K to move current window to far Up                                   |                                                                                               |
| ctrl-w L to move current window to far left                                 |                                                                                               |
| ctrl-w T to move current window to new tab                                  |                                                                                               |
| ctrl-w n to open new file in H split                                        |                                                                                               |
| ctrl-w q to close                                                           |                                                                                               |
| ctrl-w o to close all splits except current window (:only also do the same) |                                                                                               |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Registers**                                                               | **Registers**                                                                                 |
| Marking registers -                                                         | Marking registers -                                                                           |
| ma - to mark position on a                                                  | C-x r Space a - to mark position on a                                                         |
| 'a - to jump to position a                                                  | C-x r j a - to jump to position on a                                                          |
|                                                                             |                                                                                               |
| Copying & paste to registers -                                              | Copying & paste to registers -                                                                |
| "ayy - yank current line to register a                                      | C-x r s a yank selected region to register a                                                  |
| "Ayy - append current line to register a                                    | C-x r i a insert selected region                                                              |
| V"ay - in visual mode, to register a                                        | M-x view-register <CR> a to view contents of register a                                       |
| V"Ay - append current selection to register a                               | M-x append-to-register to append selected region to register a                                |
| "ap to paste content of register a                                          | M-x prepend-to-register to prepend selected region to register a                              |
| :reg to view all registers                                                  | C-x r r a to copy the rectangle area to register a                                            |
| :reg a to view contents in register a                                       | C-x r i a to paste the rectangle area to register a                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **To remove duplicate lines**                                               | **To remove duplicate lines**                                                                 |
| :sort u to remove duplicate lines                                           | Keep below functions in .emacs file                                                           |
|                                                                             | ;; To remove duplicate lines                                                                  |
|                                                                             | (defun uniquify-all-lines-region (start end)                                                  |
|                                                                             | "Find duplicate lines in region START to END keeping first occurrence."                       |
|                                                                             | (interactive "*r")                                                                            |
|                                                                             | (save-excursion                                                                               |
|                                                                             | (let ((end (copy-marker end)))                                                                |
|                                                                             | (while                                                                                        |
|                                                                             | (progn                                                                                        |
|                                                                             | (goto-char start)                                                                             |
|                                                                             | (re-search-forward "^\\(.*\\)\n\\(\\(.*\n\\)*\\)\\1\n" end t))                                |
|                                                                             | (replace-match "\\1\n\\2")))))                                                                |
|                                                                             |                                                                                               |
|                                                                             | (defun remove-duplicate-lines ()                                                              |
|                                                                             | "Delete duplicate lines in buffer and keep first occurrence."                                 |
|                                                                             | (interactive "*")                                                                             |
|                                                                             | (uniquify-all-lines-region (point-min) (point-max)))                                          |
|                                                                             |                                                                                               |
|                                                                             |                                                                                               |
|                                                                             | M-x remove-duplicate-lines                                                                    |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **To delete matching lines**                                                | **To delete matching lines**                                                                  |
| :g/<regexp>/d to delete matching lines                                      | M-< M-x delete-matching-lines RET <regexp> RET                                                |
| To delete empty lines                                                       | To delete empty lines                                                                         |
| :g/^\s*$/d                                                                  | M-< M-x delete-matching-lines RET ^ *$ RET                                                    |
|                                                                             | Note: there is space between ^ and *                                                          |
|                                                                             | or                                                                                            |
|                                                                             | M-< M-x flush-lines RET <regexp> RET                                                          |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **To delete non-matching lines**                                            | **To delete non-matching lines**                                                              |
| :v/<regexp>/d to delete non-matching lines                                  | M-< M-x delete-non-matching-lines RET <regexp> RET                                            |
|                                                                             | or                                                                                            |
|                                                                             | M-< M-x keep-lines RET <regexp> RET                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **To copy matching lines**                                                  | **To copy matching lines**                                                                    |
| :g/<regexp>/y A to copy matching lines to register a                        | M-< M-x keep-lines RET <regexp> RET                                                           |
| "ap to paste matching lines                                                 | C-x h C-x r s a copy matching lines to register a                                             |
|                                                                             | C-x r i a to paste matching lines                                                             |
|                                                                             |                                                                                               |
|                                                                             | function to copy matching lines to buffer                                                     |
|                                                                             | reference - http://stackoverflow.com/questions/2289883/emacs-copy-matching-lines              |
|                                                                             | ;; To copy matching lines to another buffer *matched*                                         |
|                                                                             | (defun copy-lines-matching (re)                                                               |
|                                                                             | "find all lines matching the regexp RE in the current buffer                                  |
|                                                                             | putting the matching lines in a buffer named *matching*"                                      |
|                                                                             | (interactive "sRegexp to match: ")                                                            |
|                                                                             | (let ((result-buffer (get-buffer-create "*matching*")))                                       |
|                                                                             | (with-current-buffer result-buffer (erase-buffer))                                            |
|                                                                             | (save-match-data                                                                              |
|                                                                             | (save-excursion                                                                               |
|                                                                             | (goto-char (point-min))                                                                       |
|                                                                             | (while (re-search-forward re nil t)                                                           |
|                                                                             | (princ (buffer-substring-no-properties (line-beginning-position) (line-beginning-position 2)) |
|                                                                             | result-buffer))))                                                                             |
|                                                                             | (pop-to-buffer result-buffer)))                                                               |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **To copy non-matching lines**                                              | **To copy non-matching lines**                                                                |
| :v/<regexp>/y A to copy non-matching lines to register a                    | M-< M-x flush-lines RET <regexp> RET                                                          |
|                                                                             | C-x h C-x r s a copy matching lines to register a                                             |
|                                                                             | C-x r i a to paste matching lines                                                             |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------|
