# Fixing terminal colors being different in tmux compared to normal sessions.

Put the following two lines into the .tmux.conf (or ~/.config/tmux/tmux.conf

```
set -g default-terminal "screen-256color"
set-option -sa terminal-features ",screen-256color:RGB"
```

Then make sure that your default shell configures the TERM environment variable
to the same value. It can be done by adding the following line into your
.zshrc

```
export TERM='screen-256color'

```


