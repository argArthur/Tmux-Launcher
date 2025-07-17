# TMUX LAUNCHER

tmux-launcher is a script that extends [tmux-sessionizer](https://github.com/ThePrimeagen/tmux-sessionizer) to launch a custom session through a session-name.tmux.conf file where you can set options for tmux and launch windows and panes and anythin that can be done in your .tmux.conf

## Session files

```tmux [filename=configs.tmux.conf]
# Set the directory for new windows (when starting the session)
set-option -g default-command "cd ~/.config; exec $SHELL"

rename-window 'vim'
send-keys -t 0 'cd ~/.config/nvim/lua/configLegal; clear' C-m

neww -n 'tmux'
send-keys -t 'tmux' 'cd ~/.config/tmux; clear' C-m

neww -n 'fish' -c ~/.config/fish
send-keys -t 'fish' 'cd ~/.config/fish; clear' C-m

neww -n 'term'
```

theese files are located in ./sessions
