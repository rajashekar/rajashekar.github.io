<!--
.. title: Tmux
.. slug: tmux
.. date: 2021-04-27 13:16:41 UTC-07:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
-->

<img src="/images/command-line.jpeg" style="display: block;margin-left: auto;margin-right: auto;"><br>
---
<!-- TEASER_END -->
With Tmux you can manage multiple sessions/terms & navigate quickly. <br>
# Table of Contents
- [From Terminal to tmux](#from-terminal-to-tmux)
- [Inside tmux](#inside-tmux)
    - [Sessions](#sessions)
    - [Windows](#windows)
    - [Panes](#panes)
    - [Buffers](#buffers)
- [Plugin Manager](#plugin-manager)
    - [Installing tpm](#installing-tpm)
    - [Installing plugins](#installing-plugins)
    - [Uninstalling plugins](#uninstalling-plugins)

## From Terminal to tmux  
  - To create new session `tmux new -s sesson-name`  
  - To kill session `tmux kill-ses -t session-name`  
  - To re-attach to previous session `tmux a`. To specific session `tmux a -t session-name`  
  - To list all tmux sessions - `tmux ls`  

## Inside tmux  
Note that default prefix is `ctrl + b`, you can change this in tmux.conf - <br>
```bash
unbind C-b
set -g prefix C-a
bind C-a send-prefix
```
  - Show all shortcuts `ctrl + a ?`  
  - ### Sessions  
    - `:new -s newsession` to create new session  
    - `ctrl + a )`  go to next session  
    - `ctrl + a (`  go to previous session  
    - `ctrl + a s` show all sessions  
    - `ctrl + a $` rename session  
    - `ctrl + a d` exit tmux session go back to terminal  
      - `tmux a` to re attach to session  
      - `tmux a -t session-name` to attach to specific session  
  - ### Windows  
    - `ctrl + a c` create new window  
    - `ctrl + a ,` rename window   
    - `ctrl + a & ` kill window   
    - `ctrl + a ctrl + w` display all sessions and windows  
    - `ctrl + a ctrl + l` move to next window in current session  
    - `ctrl + a ctrl + h` move to previous window in current session  
  - ### Panes  
    - `ctrl + a %` create vertical pane  
    - `ctrl + a "` create horizontal pane  
    - `ctrl + a x` kill pane  
    - `ctrl + a space` re-arrange panes  
    - `ctrl + a ;` toggle between panes  
    - `ctrl + a o` move to next pane  
    - `ctrl + a l` - move right, `ctrl + a h` - move left  
    - `ctrl + a j` move up, `ctrl + a k` move down    
    - `ctrl + a z` zoom to pane (toggle)  
    - `ctrl + a !` convert pane to window  
  - ### Buffers  
    - `ctrl + a #` list buffers  
    - `ctrl + a =` list buffers to copy  
      - `/` to search in buffers  
    - `: capture-pane` capture visibile details in buffer  
    - `:save-buffer buf.txt` to save   
  - Copy Mode `ctrl + a ESC`  
  - Command Mode `ctrl + a :`  
  - `:setw setw synchronize-panes` Synchronize panes  

## Plugin Manager
You can use [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) to handle your tmux plugins
### Installing tpm
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```  
Put this at the bottom of ~/.tmux.conf ($XDG_CONFIG_HOME/tmux/tmux.conf works too):  
### Installing plugins
- Add new plugin to ~/.tmux.conf with set -g @plugin '...'  
- Press prefix + I (capital i, as in Install) to fetch the plugin.  
- You're good to go! The plugin was cloned to ~/.tmux/plugins/ dir and sourced.  
```bash
# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Other examples:
# set -g @plugin 'github_username/plugin_name'
# set -g @plugin 'git@github.com:user/plugin'
# set -g @plugin 'git@bitbucket.com:user/plugin'
```

Type this in terminal if tmux is already running
```bash
tmux source ~/.tmux.conf  
```
### Uninstalling plugins  
- Remove (or comment out) plugin from the list.  
- Press prefix + alt + u (lowercase u as in uninstall) to remove the plugin.  
- All the plugins are installed to ~/.tmux/plugins/ so alternatively you can find plugin directory there and remove it.  
