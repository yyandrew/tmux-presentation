Hello everyone welcome to Creative Friday.Today I will introduce you a cool tool .It's tmux~~~.Does anybody know tmux?

# What is tmux

Tmux authors describe it as a terminal multiplexer.

It enables a number of windows to be created, accessed, and controlled from a single window terminal.

Maybe some of you are using iterm, terminal.

When tmux is started it creates a new session within a single window and displays it on screen.

Simply speaking tmux acts as a window manager within your terminal and allow you to create multiple windows and panes within a single terminal window.

A status line at the bottom of the screen shows information on the current session and it used to enter interactive commands

# Tmux config
Using the config files, lots can be customized. /etc/tmux.conf $HOME/.tmux.conf Session intialization Layout and colors of all status bar items Extending status bar with shell scripts Keyboard shortcuts / macros General behaviour of tmux Too much to mention here

# Session
A session is a pseudo terminals under the manangement of tmux.Session are useful for completely separating work environments.For example, I have a 'Work' session and a 'Play' session.In 'Work' session, I keep everything open what I need during my day-to-day development.While in 'Play' session I keep open current open-source gems or other work I hack on at home.

Each session is persistent and will servive accidental disconnection(such as ssh connection timeout) or intentional detaching(with the <prefix> d key strokes).`tmux will may be reattached using tmux attach)

# Windows
Tmux has a tabbed interface. but it calls its tabs 'Windows'.To stay organized.I usually rename all the window I use;If I am coding, I will name the window `vim`, If i am debug I will name the window `rails s`

# Key bindings

`tmux` may be controlled from an attached client by using a key combination of a prefix key. `C+b` by default
## Diffence between tmux and screen

* Some reasons I prefer tmux over screen

1, Status bar is much easier to use.
2, Choice of vi or emacs key layouts
3, Much more accurate automatic window renaming
4, Nicer session handling. You can do a lot more with sessions within tmux itself. You can easily switch, rename, etc

one big problem of `screen` is it is not actively developed,The [bug pages](https://savannah.gnu.org/bugs/?group=screen&func=browse&set=open&msort=0&advsrch=0&morder=bug_id%3C&offset=0#results) have close to 200 unassigned items going back over 5 years.
