# Darkcloud TMUX Config

## Features

* A custom theme that matches the one used in [darkcloud-vimconfig](https://github.com/prurigro/darkcloud-vimconfig).
* A bandwidth monitor showing the current upload and download speed of either **eth0** or the device you've set to **$NETDEV**.
* Sane defaults and a set of custom key bindings that group similar ideas and make frequently used commands easier to access.
* Optional support for powerline fonts that looks oh so much better when they're used :).

![Darkcloud TMUX Config Theme](https://i.imgur.com/Ps3XmMc.png)

## Installation

1. Choose either **tmux.powerline.conf** if powerline fonts are available or **tmux.normal.conf** if they're not, and install it to __/etc/tmux.conf__ for a system-wide install or __~/.tmux.conf__ for a local install.
1. Install **bwrate** to somewhere available in **$PATH** and make it executable (ie: `install -Dm755 bwrate /usr/local/bin/bwrate`)
1. If your network device isn't named **eth0**, set **$NETDEV** to the name of the device you'd like to use somewhere tmux will see it when it runs (ie: `echo 'export NETDEV="wlan0"' >> ~/.bashrc`)

## Key Bindings

* **Prefix**: `<Ctrl><Space>`

| Key(s)                                  | Behaviour                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------|
| `c` and `<Ctrl>c`                       | Create a new pane and create a new pane in the current directory respectively          |
| `[` and `]`                             | Split the window vertically and horizontally respectively                              |
| `-` and `=`                             | Select an even layout vertically and horizontally respectively                         |
| `_` and `+`                             | Rotate the window counter-clockwise and clockwise respectively                         |
| `S`                                     | Run the `swap-pane` command to swap the current pane with the marked one               |
| `.` and `,`                             | Move and swap the current window with the provided window number respectively          |
| `$` and `#`                             | Rename the current session and window with the provided name respectively              |
| `<Space>` and `<Ctrl><Space>`           | Move to the previously selected pane and window respectively                           |
| `h`, `j`, `k` and `l`                   | Move left, down, up and right between panes respectively like the arrow keys           |
| `` ` ``                                 | Toggle synchronized input between the panes on the current window                      |
| `<Ctrl>r`                               | Clear the terminal history, tmux history and the current window/pane                   |
| `r` and `R`                             | Reload /etc/tmux.conf and ~/.tmux.conf respectively                                    |
| `?` and `/`                             | Show help for available key bindings and commands respectively                         |
| `y` and `<Ctrl>p`                       | Enter __copy mode__ and paste from the copy buffer respectively                        |
| `<Ctrl>v` and `<Ctrl>y`                 | Pastes the X buffer in tmux, and sends the tmux buffer to X respectively               |
| (**copy mode**) `v`, `y` and `<Escape>` | Begin selection, copy selection and cancel **copy mode** respectively                  |
| `W`                                     | Write scrollback buffer to file                                                        |
| `Alt-[0-9]` (no prefix)                 | Switch directly to the given window                                                    |

## Credits

* Written by Kevin MacMartin: [GitHub Projects](https://github.com/prurigro) | [Arch Linux AUR Packages](https://aur.archlinux.org/packages/?SeB=m&K=prurigro)

## License

This config and the bwrate script are released under the MIT license.
