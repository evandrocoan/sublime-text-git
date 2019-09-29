[![Build Status](https://travis-ci.org/kemayo/sublime-text-git.svg?branch=master)](https://travis-ci.org/kemayo/sublime-text-git)
# Sublime Text plugin: git

Git integration: it's pretty handy. Who knew, right?

For more information about what's supported, and how to install this, [check the wiki](https://github.com/kemayo/sublime-text-git/wiki).


## Installation

### By Package Control

1. Download & Install `Sublime Text 3` (https://www.sublimetext.com/3)
1. Go to the menu `Tools -> Install Package Control`, then,
   wait few seconds until the `Package Control` installation finishes
1. Go to the menu `Preferences -> Package Control`
1. Type `Package Control Add Channel` on the opened quick panel and press <kbd>Enter</kbd>
1. Then, input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Now, go again to the menu `Preferences -> Package Control`
1. This time type `Package Control Install Package` on the opened quick panel and press <kbd>Enter</kbd>
1. Then, search for `Git` and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


### Basic Usage

 * Bring up the Command Palette (Command+Shift+p on OS X, Control+Shift+p on Linux/Windows).
 * Start typing "Git" and select one of the recommended commands.

### The rest

If you don't want to use Package Control, [check the wiki](https://github.com/kemayo/sublime-text-git/wiki) for other installation methods on various platforms.

## Troubleshooting

This package works by running commands as your system `git`. As such, if you have problems with this package, first make sure that git is installed and configured correctly on your system.

You may want to make sure that the `git` binary this plugin is using is the correct one, if you have multiple ones installed. Most git installation guides will be happy to walk you through configuring your system `$PATH` appropriately.

If necessary, set the `git_command` plugin preference to tell us where to look.

### `fatal: unable to auto-detect email address`

Git isn't configured properly. Tell it who you are, by opening a command prompt and doing this:

    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"

If you've done this and it's still complaining, you probably have multiple copies of git on your system which have different configuration locations, and the one which runs on your command line isn't the one which the shell `$PATH` exposes to Sublime Text.

### `fatal: could not read Username for 'https://github.com': Device not configured`

Git isn't configured to use a system-level ssh-agent, and so it's asking you for a username and password when you try to push / pull. The plugin doesn't know how to ask you for this information.

[Set up a ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent) and this will stop happening.

## Acknowledgements

This package contains:

* [Sublime Text git Commit Message Syntax](https://github.com/adambullmer/sublime_git_commit_syntax) by [Adam Bullmer](https://github.com/adambullmer).
