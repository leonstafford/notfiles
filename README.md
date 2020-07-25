# notfiles

Not my dotfiles, just the minimal adjustments to a freshly installed OpenBSD workstation

### Vim

```
set ts=2 sw=2 expandtab ruler nu noswapfile colorcolumn=80                      
syntax on                                                                       
colorscheme delek                                                               
                                                                                
autocmd Filetype php setlocal expandtab tabstop=4 shiftwidth=4 softtabstop=4       
autocmd Filetype js setlocal expandtab tabstop=2 shiftwidth=2 softtabstop=2
```

### Tmux

```
# moving between panes
bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R

# large history limit
set -g history-limit 999999999
```

### ksh

```
# $HOME/.profile
# disable bell in xterm (still needed after Xdefaults edits?)
xset b off
```

### xterm

```
! $HOME/.Xdefaults
xterm*loginShell:true                                                                                                                                       
xterm*background: black                                                         
xterm*foreground: lightgreen                                                    
xterm*scrollBar: false                                                          
xterm*visualBell: false 
```



Originally scattered around web like https://leonstafford.github.io/notes/keep_your_core_strong_know_your_bsd_linux_tools/
