Hello everybody welcome to Creative Friday.Today I will introduce you a useful tool.It's tmux. Does anybody know tmux?

I use tmux almost every single day.I will show you why I think it is awsome.
Normally in most cases when you have work going on inside a terminal and you accidentally close it and your work is gone you pretty much lost everything that you are working on.I mean I am working on a ruby script that I put a lot of time in that, I forgot to save or you know maybe some process was running that I really need to finish and I just accidentally closed the window, that's not a good day for most people.On the other hand if you are using tmux this will never happen.
Let me show the magic.First I create a tmux session with command `tmux`.Then use `top` to show the process which running on my computer.And create an other panes by `<prefix> + %` run cowsay `Hello Tmux`, and create the third panes run `vim test.rb`.Then detach the session and close the terminal.Then open a new terminal.And you can notice here it's just an empty shell right so if I do a `tmux a` for attach press `Enter` there it is, My workflow is back.And this is the reason why I love it. Because even though I disconnnect from this tmux session tmux is still running on my computer so it's basically keeping my session alive in the background and I could connect to it and disconnect to it anytime i want.And that's one of the things i love most about it especially for those of you that work that actually use terminal a lot as i do at my day job.
Don't worry about not knowing what i am doing here and commands that i excuted it here.

In this presentation I will show you what tmux is and how to use it.

# What is tmux

Tmux authors describe it as a terminal multiplexer.A terminal multiplexer is a software application that can be used to multiplex several virtual consoles, allowing a user to switch easily bewtween multiple programs and separate terminal sessions inside a single terminal window or remote terminal session.

It enables a number of windows to be created, accessed, and controlled from a single window terminal.

Simply speaking tmux acts as a window manager within your terminal and allow you to create multiple windows and panes within a single terminal window.

# What does it look like?

A status line at the bottom of the screen shows information on the current session.

Maybe some of you are using iterm, terminal.But tmux has some special features they don't have and it is more powerful.Detach sesion and reattech session, status bar, choice of vi or emacs key layouts and so on.


# Installation

# Main Structure

# Prefix

[youtub](https://youtu.be/FEfuXRTqINg?t=21s).Before we go forther there is one requirement that i have to tell you first and that's known as the *prefix*.Understanding the tmux *prefix* is a single most important thing because it's where everything in tmux begins so by default the *prefix* which is basically just a keyboard shortcuts is `ctrl + B` so you hold ctrl and press letter B on your keyboard and what the *prefix* does is it says to tmux hi tmux i want you to do something and tmux listens for you to press another buttom on the keyboard and corresponds with an action that you want to to take.Now I am going to give you some examples next.

# Session
A session is a pseudo terminals under the manangement of tmux.A session holds on or more windows.Sessions are useful for completely separating work environments.

For example, I have a 'SONAR' session and a 'Pipeline' session.In 'SONAR' session, I keep everything open what I need during "SONAR" development.While in 'Pipeline' session I keep open "Pipeline" development

----Each session is persistent and will servive accidental disconnection(such as ssh connection timeout) or intentional detaching(with the <prefix> d key strokes).`tmux will may be reattached using tmux attach)----

# Windows
Tmux has a tabbed interface. but it calls its tabs 'Windows'.To stay organized.I usually rename all the window I use;If I am coding, I will name the window `vim`, If i am debug I will name the window `rails s`

# Panes

Panes is a rectangular part of a window that runs a specific command (e.g., Bash, Zsh). They reside within a window. A terminal within a terminal, they can run shell commands, scripts, and programs, like vim, emacs, top, htop, rails server, rails console, and so on within them.

To create a new pane, you can split-window from within the current window and pane you are in.

## Sync tmux panes

By using synchronize-panes window option you can send each pane the same keyboard input simultaneously.
You can do this by switching to the appropriate window, typing your Tmux prefix (commonly Ctrl-B) and then a colon to bring up a Tmux command line, and typing:
```sh
:setw synchronize-panes
```

You can optionally add *on* or *off* to specify which state you want; otherwise the option is simply toggled. This option is specific to one window, so it won’t change the way your other sessions or windows operate. When you’re done, toggle it off again by repeating the command.

This is an easy way to run interactive commands on multiple machines, perhaps to compare their speed or output, or if they have a similar setup a quick and dirty way to perform the same administrative tasks in parallel.

# Tmux config
Using the config files, lots can be customized. /etc/tmux.conf $HOME/.tmux.conf Session intialization Layout and colors of all status bar items Extending status bar with shell scripts Keyboard shortcuts / macros General behaviour of tmux Too much to mention here

# Key bindings

`tmux` may be controlled from an attached client by using a key combination of a prefix key. `C+b` by default.As i mentioned here default means you can change the prefix key by you self.

## Diffence between tmux and screen

### Some reasons I prefer tmux over screen

1, Status bar is much easier to use.

2, Choice of vi or emacs key layouts.

3, Much more accurate automatic window renaming.

4, Nicer session handling. You can do a lot more with sessions within tmux itself. You can easily switch, rename, etc

one big problem of `screen` is it is not actively developed,The [bug pages](https://savannah.gnu.org/bugs/?group=screen&func=browse&set=open&msort=0&advsrch=0&morder=bug_id%3C&offset=0#results) have close to 200 unassigned items going back over 5 years.
