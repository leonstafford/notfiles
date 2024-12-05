# notfiles

Not my dotfiles, just the minimal adjustments to a freshly installed OpenBSD/Linux workstation

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
xterm*faceName: Monospace
xterm*faceSize: 10
```

### .cwmrc

```
# Bind the keys with the Super modifier - reload with CMS-r
bind-key CM-1 "jumpapp firefox"
bind-key CM-2 "jumpapp chromium-browser"
bind-key CM-3 "jumpapp code"
# bind-key CM-grave "sh -c 'wmctrl -a leon@leon || x-terminal-emulator'"
bind-key CM-Escape "sh -c 'wmctrl -a leon@leon || x-terminal-emulator'"
bind-key CM-4 "jumpapp telegram-desktop"
bind-key CM-5 "jumpapp slack"
bind-key CM-6 "jumpapp discord"
bind-key CM-7 "jumpapp parsecd"
bind-key CM-0 "jumpapp postman"
bind-key CM-Return "x-terminal-emulator"
```

### xmodmap (funky keyboard)

`xmodmap ~/.xmodmaprc` in `~/.xinitrc` etc

```
clear Lock
keysym Caps_Lock = grave asciitilde
```

Originally scattered around web like https://leonstafford.github.io/notes/keep_your_core_strong_know_your_bsd_linux_tools/
