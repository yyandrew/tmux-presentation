Hello everybody welcome to Creative Friday.Today I will introduce you a useful tool .It's tmux. Does anybody know tmux?


I will show you why I like it.I am going to go ahead and close my window.So normally in most cases when you have work going on inside a terminal and you accidentally close it and your work is gone you pretty much lost everything that you are working on.I mean i am working on a ruby script that i put a lot of time in that i forgot to save or you know maybe some process was running that i really need to finish and i just accidentally closed the window that's not a good day for most people but what you can do with tmux if you use tmux.Let me show the magic.First I create a tmux session with command `tmux`.Then use `top` to show the process which running on my computer.And create an other panes by `<prefix> + %` run cowsay `Hello Tmux`, and create the third panes run `vim test.rb`.Then detach the session and close the terminal.Then open a new terminal.And you can notice here it's just an empty shell right so if I do a `tmux a` for attach
press `Enter` there it is my workflow is backAnd the reason why is because even though i disconnnect form this tmux session tmux is still running on my computer so it's basically keeping my session alive in the background and i coulse connect to it and disconnect to it anytime i want.And that's one of the things i love most about it especially for those of you that work that actually use terminal a lot as i do at my day job.There is a lot of other reasons to use tmux.Don't worry about not knowing what i am doing here any commands that i am excute it here.In the next part I  will show you more about tmux.

In this presentation I will show you what tmux is and how to use it.

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

2, Choice of vi or emacs key layouts.

3, Much more accurate automatic window renaming.

4, Nicer session handling. You can do a lot more with sessions within tmux itself. You can easily switch, rename, etc

one big problem of `screen` is it is not actively developed,The [bug pages](https://savannah.gnu.org/bugs/?group=screen&func=browse&set=open&msort=0&advsrch=0&morder=bug_id%3C&offset=0#results) have close to 200 unassigned items going back over 5 years.
