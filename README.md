# fish_abbreviations
Useful fish abbreviations I've collected

Fish abbreviations are autocomplete shortcuts that make for an excellent alternative to the standard function. Abbreviations are recommended because they effectively change nothing; you're merely referencing functions which already exist.

Abbreviations can be added from the fish prompt by typing `abbr` followed by the variable you wish to designate as the shorthand, and finally the command, text, directory etc you want to abbreviate. The abbreviated command can be wrapped in quotes to include multiple commands. (If no options are included with 'abbr', fish will assume the '-a' option, adding the abbreviation.) Once added the abbreviation will expand after typing the variable and hitting the spacebar. 

Example: 

`$ abbr itchdir 'cd /home/kendofriendo/.config/itch/apps/'`

Now 'itchdir' and a space becomes `$ cd /home/kendofriendo/.config/itch/apps/`

I know have a handy dandy abbreviation to get to my itch.io apps folder. While some directories are somewhat easy to remember like this, once you've got a few dozen or more convoluted directories this is really a lifesaver. 

You can see how fish interpreted the command to create the abbreviation by typping `abbr -s`

`> abbr -a -U -- itchdir 'cd /home/kk/.config/itch/apps/'

You can also use this option to quickly get a list of all of your abbreviations for backups and migrations. The stdout can be copied and pasted as is to migrate your abbreviations!

Addtitionally, `abbr -e` to remove an abbreviation, or `abbr -r` to rename an existing abbreviation (eg `abbr -r itchdir itchd`). The rename feature is quite nice since can set and forget lengthy commands and paths and rename them if they become inconvenient without having to look them up again.

Lastly, if you have access to 20th century technological innovations like a Graphical Processing Unit, you can view, add, edit, and delete your fish abbreviations by using fish's built-in `fish_config`.

Feel free to ping with your suggestions, fork, submit a pull request, or hurl insults at me.
