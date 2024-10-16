# Darkcloud TMUX Config

## Features

* A custom theme that matches the one used in [darkcloud-vimconfig](https://github.com/prurigro/darkcloud-vimconfig).
* A bandwidth monitor showing the current upload and download speed of either **eth0** or the device you've set to **$NETDEV**.
* Sane defaults and a set of custom key bindings that group similar ideas and make frequently used commands easier to access.
* Optional support for powerline fonts that looks oh so much better when they're used :).

![Darkcloud TMUX Config Theme](https://i.imgur.com/Ps3XmMc.png)

## Installation

1. Choose either `tmux.powerline.conf` if powerline fonts are available or `tmux.normal.conf` if they're not, and install it to __/etc/tmux.conf__ for a system-wide install or __~/.tmux.conf__ for a local install.
1. Install **bwrate** to somewhere available in `$PATH` and make it executable (ie: `install -Dm755 bwrate /usr/local/bin/bwrate`)
1. If your network device isn't named `eth0`, set `$NETDEV` to the name of the device you'd like to use somewhere tmux will see it when it runs (ie: `echo 'export NETDEV="wlan0"' >> ~/.bashrc`)

## Key Bindings

* **Prefix**: `<Ctrl><Space>`

### With Prefix

| Key(s)                                  | Behaviour                                                          |
|-----------------------------------------|--------------------------------------------------------------------|
| `c` and `<Ctrl>c`                       | Create a new pane and create a new pane in the current directory   |
| `[` and `]`                             | Create a new pane to the right and below the current one           |
| `-` and `=`                             | Select an even layout vertically and horizontally                  |
| `_` and `+`                             | Rotate the panes clockwise and counter-clockwise                   |
| `S`                                     | Swap the current pane with the marked one (`M` to mark)            |
| `,`                                     | Swap the current window with another (using its index)             |
| `#`                                     | Rename the current window                                          |
| `<Space>` and `<Ctrl><Space>`           | Move to the previously selected pane and window                    |
| `` ` ``                                 | Toggle synchronized input between the panes on the current window  |
| `r` and `R`                             | Reload /etc/tmux.conf  and ~/.tmux.conf                            |
| `F1` and `F2`                           | Show help for available commands and keyboard bindings             |
| `W`                                     | Write scrollback buffer to file                                    |
| `V`                                     | Enter **copy mode**                                                |
| `<Ctrl>p`                               | Paste from the copy buffer                                         |
| `P` and `N`                             | Move to the previous and next session                              |

### Without Prefix

| Key(s)                                  | Behaviour                                                          |
|-----------------------------------------|--------------------------------------------------------------------|
| `<Alt><Up,Down,Left,Right>`             | Navigate to the pane in the respective direction                   |
| `<Alt>n` and `<Alt>p`                   | Switch to the next and previous window                             |
| `<Ctrl><Alt>n` and `<Ctrl><Alt>p`       | Swap the current window with the next and previous window          |
| `Alt-[0-9]`                             | Switch to the window with the respective index                     |
| `Alt-?`                                 | Start searching up                                                 |

### Copy Mode

| Key(s)                                  | Behaviour                                                          |
|-----------------------------------------|--------------------------------------------------------------------|
| `v`                                     | Start visually selecting text                                      |
| `y`                                     | Copy the selected text                                             |
| `<Escape>`                              | Exit **copy mode**

## Credits

* Written by Kevin MacMartin: [GitHub Projects](https://github.com/prurigro) | [Arch Linux AUR Packages](https://aur.archlinux.org/packages/?SeB=m&K=prurigro)

## License

This config and the bwrate script are released under the MIT license.
