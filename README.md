# wsl_terminal
This package allows you to execute commands in the WSL terminal via Python 3. There are some tools that I use that require the use of Linux. I decided to just run these through the Windows Subsystem for Linux (WSL) with the use of Python. I could not find a method of performing this the way I wanted, but I did find a solution for Python 3 [here](https://github.com/skywind3000/terminal). However, there was no Python 3 support. I essentially converted that package to Python 3 and only kept the WSL portions of the code.

# Usage

My general usage is something like the following. This example will perform a list of commands (command1, and command2) within the WSL terminal. The profile and the title parameters are legacy from the code that I converted. I have no use for them. I assume the profile command would log you into a specific profile, have not tested it though.

```
from wsl_terminal import BashConfigure

profile = None
title = None
cfg = BashConfigure()
cfg.win32_wsl_open_bash(title, ['command1', 'command2'], profile)
```
