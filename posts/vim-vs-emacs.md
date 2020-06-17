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

| VIM                                               |  EMACS                                              |
|---------------------------------------------------|-----------------------------------------------------|
|---------------------------------------------------|-----------------------------------------------------|
| Navigation                                        | Navigation                                          |       
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
| Undo                                              |  Undo                                               |
| u - undo                                          | C-_ or C-x u or C-z to undo                         |
|---------------------------------------------------|-----------------------------------------------------|
| Search                                            |  Search                                             | 
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
|---------------------------------------------------|-----------------------------------------------------|