<div align="center">
  <!-- PR's Welcome -->
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square"
      alt="PR's Welcome" />
  </a>
</div>

 <h1 align="center">Jarvis</h1>

<div align="center">
  <strong>(Neo)Vim of the Future</strong>
</div>
<div align="center">
  A powerful development environment with cutting-edge features
</div>

## Table of Contents
- [Features](#features)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Commands](#commands)
- [Support](#support)

## Features

The following are features provided by Jarvis. They all have quick keybindings to make them quick and easy to use.

1. **Quick-open files** - *zsh* & *NeoVim*

    Open files with simple keystrokes with fuzzy matching via command line and inside NeoVim.

    <img src="https://media.giphy.com/media/xUOxeZpELYRSECCZR6/giphy.gif"/>

2. **Buffer management** - *NeoVim*

    Manage buffers inside NeoVim and add/delete/search your open files.

    <img src="https://media.giphy.com/media/xT0xejSMJ76K68Nf0c/giphy.gif"/>

3. **Project searching** - *NeoVim*

    Quickly search for simple terms or complex regular expressions in your project.

    <img src="https://media.giphy.com/media/3oxHQpx3kxuUk2oa40/giphy.gif"/>

4. **Asynchronous linting** - *NeoVim*
5. **Session management** - *Tmux*

    Create sessions for each project with a custom layout. Quickly browse, create, and delete sessions. Tmux even keeps sessions alive if the terminal is closed.

6. **Keyword auto-complete** - *NeoVim* and *zsh*

    Neovim - Automatic, asynchronous keyword completion available in the current buffer via [deoplete](https://github.com/Shougo/deoplete.nvim).

    **Supported Languages**
    * Javascript - support provided by [deoplete-ternjs](https://github.com/carlitux/deoplete-ternjs) and [TernJS](http://ternjs.net/).
    * Vimscript - support provided by [neco-vim](https://github.com/Shougo/neco-vim)


    zsh - Command completion provided by zsh plugins.

7. **Code Snippets** - *NeoVim*

    Commonly used code snippets made available with a few keystrokes to reduce time and effort. Snippets available via auto-complete window removes need to memorize commands.

8. **Improved JS and JSDoc syntax highlighting** - *NeoVim*
9. **Powerful Git integration** - *zsh* & *NeoVim*
10. **Clean, customizable UI** - *zsh* & *NeoVim*
11. **Improved Vim motion** - *NeoVim*
12. **Extensive documentation** - *Neovim*, *zsh*, & *tmux*

    Each configuration file is thoroughly documented to make each setting easy to understand.

## Dependencies

The following tools are the only ones that are required to be installed manually (if you are using OSX). 

1. [iTerm2](https://www.iterm2.com/) - Terminal emulator for macOS.

2. [iTerm2 Oceanic Theme](https://github.com/mhartington/oceanic-next-iterm) - Oceanic theme for Iterm. Provies seamless UI experience between Neovim + Tmux.

    Manually update your iTerm setup to use the new font (*Knack Regular Nerd Font Complete* is added by the installation script) and colorscheme.

## Installation

Clone Jarvis into your directory of choice and run the install script. This script will install [Homebrew](https://brew.sh/) (if it needs to) and then install all of Jarvis' dependencies. 

**Warning: This will move existing `zsh`, `tmux`, or `nvim` configurations to a backup folder inside of the installation repo.**

*Note: If you are on another OS, then you will have to install the supported plugins yourself. No guarantees on compatibility issues.*

```
git clone https://github.com/ctaylo21/jarvis ~/jarvis
cd ~/jarvis
./install.sh
```
**Installed Tools**

1. [Tmux](https://github.com/tmux/tmux/wiki) - Terminal multiplexer with session management, customizable terminal layouts, and much more.

2. [NeoVim](https://github.com/neovim/neovim) - A fork of Vim that was created to be a community-driven rewrite of Vim that is focused on cleaning up the codebase and providing a way for developers to contribute to the advancement of the editor. For a list of all the plugins installed for Neovim, see the [plugins file](config/nvim/plugins.vim).

3. [Python 3](https://www.python.org/downloads/)/[Python Neovim Client](https://github.com/neovim/python-client) - Implements support for python plugins in Neovim.

4. [ripgrep](https://github.com/BurntSushi/ripgrep) - A blazingly fast line-oriented search tool that respects .gitignore rules.

5. [fzf](https://github.com/junegunn/fzf#installation) - A general-purpose command-line fuzzy finder that can be used with any list; files, command history, processes, hostnames, bookmarks, git commits, etc.

6. [z](https://github.com/rupa/z) - Tracks your most used directories and lets you quickly hop there with regexes.

7. [nerd font](https://github.com/ryanoasis/nerd-fonts#font-installation) - Custom fonts with glyphs added for icon support within NeoVim.

8. [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) - Installs and loads tmux plugins.

## Commands

The following are the custom commands in Jarvis and some of the most useful default ones. Each configuration file is carefully documented to make it easy to understand. Many default commands for each tool may not be listed.

### Neovim Commands

| Command      | Mode           | Tool          | Description                                           |
| :---         | :---           | :---          |:---                                                   |
| `<Space>`    | normal         | NeoVim        | Page down                                             |
| `-`          | normal         | NeoVim        | Page up                                               |
| `<leader>h`  | normal         | NeoVim        | Find and replace                                      |
| `<leader>/`  | normal         | NeoVim        | Clear highlighted search terms                        |
| `<leader>f`  | normal         | NERDTree      | Find current file in tree hiearchy                    |
| `<leader>n`  | normal         | NERDTree      | Toggle NERDTree window                                |
| `C`          | normal     *NT*| NERDTree      | Switch NERDTree root to be directory under cursor     |
| `;`          | normal         | Denite        | Browse currently open buffers                         |
| `<leader>t`  | normal         | Denite        | Browse files in current directory                     |
| `<leader>g`  | normal         | Denite        | Search current directory for occurences of term       |
| `<leader>j`  | normal         | Denite        | Search current directory for word under cursor        |
| `<c-o>`      | insert         | Denite        | Switch to normal mode (useful inside *DW*)            |
| `d`          | normal     *DW*| Denite        | Delete item (can delete open buffer inside *DW*)      |
| `<leader>y`  | normal         | vim-better-whitespace        | Remove trailing whitespace in file     |
| `<leader>w`  | normal         | EasyMotion    | Highlight first letter of file words for quick move   |
| `<TAB>`      | insert    *AWV*| Deoplete      | Moves inside of auto-complete window if it's open     |
| `<c-n>`      | normal    *AWV*| Deoplete      | Moves to next suggested auto-complete term            |
| `<c-p>`      | normal    *AWV*| Deoplete      | Moves to previous suggested auto-complete term         |
| `<c-k>`      | insert    *AWV*| NeoSnippet    | Activates first valid snippet that matches            |
| `<TAB>`      | insert     *SP*| NeoSnippet    | Move to next available field of snippet               |
| `<TAB>`      | select     *SP*| NeoSnippet    | Move to next available field of snippet               |

<br />

* *DW*  - Within Denite window
* *NT*  - Within NERDTree window
* *AWV* - With auto-complete window visible
* *AW*  - Inside auto-complete window
* *SP*  - Inside of snippet

### Tmux Commands
Below are some custom key mappings as well as some default tmux commands. Not all tmux commands are included,
just some of the more common ones in my workflow.

#### Prefix Mappings
| Command          | Description                                                        |
| :---             | :---                                                               |
| `<c-a>I`         | Install tmux plugins                                               |
| `<c-a>(h/j/k/l)` | Switch Tmux panes (left/down/up/right)                             |
| `<c-a>(H/J/K/L)` | Resize Tmux panes based on current pane (left/down/up/right)       |
| `<c-a>-`         | Create split horizontally                                          |
| `<c-a>`&#124;    | Create split vertically                                            |
| `<c-a>x`         | Close pane                                                         |
| `<c-a>$`         | Rename session                                                     |
| `<c-a>s`         | Browse open sessions - navigate with h/j/k/l and enter to select   |
| `<c-a>z`         | Full-screen the current pane                                       |

#### Tmux Command Line
All of the following command are triggered by `<c-a>:` (Note the colon)

| Command               | Description                                                        |
| :---                  | :---                                                               |
| `new -s test`         | Create new session named "test"                                    |
| `kill-session -t test`| Delete session named "test"                                        |

## Miscellaneous Configuration

The following configurations require changes outside of Jarvis.

### Mapping Caps Lock to Escape

In order to keep your fingers near the home row, mapping caps lock to escape to get out of different vim modes can be extremely helpful.

This can be done on MacOS by following these simple steps: http://vim.wikia.com/wiki/Map_caps_lock_to_escape_in_macOS

This is especially useful for laptops that made the escape key "virutal" (*I'm looking at you, Apple*).

## Support

If you find any problems or bugs, please open a new [issue](https://github.com/ctaylo21/jarvis/issues).
