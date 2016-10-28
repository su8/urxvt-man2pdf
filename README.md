Convert man page while reading it to pdf in urxvt.
No need to quit reading or open another terminal instance/tab.
Bind the desired keyboard shortcut and this extension will do all the heavy lifting for you.

![](https://cloud.githubusercontent.com/assets/4725121/16555529/6e02ec1c-41d5-11e6-9ca6-1009de85e11a.png)

# Installation

Simply place the script in **/usr/lib/urxvt/perl/** for
system-wide availability or in **~/.urxvt/ext/** for user-only availability.
You can also put it in a folder of your choice, but then you have to add this
line to your **.Xdefaults/.Xresources**:

```bash
# Don't type ~ or $HOME below
URxvt.perl-lib: /home/user/your/folder/
```

After installing, put the following lines in your **.Xdefaults/.Xresources**:

```bash
# libs to activate, do not omit selection-to-clipboard
URxvt.perl-ext-common           : man

# keyboard shortcut to trigger the lib
URxvt.keysym.Control-Shift-X    : perl:man:topdf
```

# Requirements

* libnotify (to let you know when convesion begins)
* ghostscript
