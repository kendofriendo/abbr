# fishbubbles
Fish Shell abbreviations I've created or collected.

## About Abbreviations
In fish, abbreviations are autocompleting text-expansion shortcuts that make for an excellent alternative to the standard shell function. When possible it's a good idea too use abbreviations over functions, because it keeps the environment clean and prevents possible collisions. Use functions when you need to run your commands as part of a script, or you need more function-ality.

As of version 3.6.0, you have to set abbreviations in your config.fish file in order to ensure they persist between sessions.

Abbreviations are added with `abbr -a` followed by the variable you wish to designate as the shorthand, and finally the command, text, directory etc you want to abbreviate. The abbreviated command can be wrapped in quotes to ensure it is contained in that single abbreviation.

Abbreviations for the current session can be added from the fish prompt by typing `abbr`. If no options are included with 'abbr', fish will assume the '-a' option for 'add.'

Example: 

```fish
#~/.config/fish/config.fish

abbr itchdir 'cd /home/kendofriendo/.config/itch/apps/'
```

Now 'itchdir' and a space becomes
```fish
cd /home/kendofriendo/.config/itch/apps/
```

I now have a handy dandy abbreviation to get to my itch.io apps folder. While some directories are somewhat easy to remember like this, once you've got a few dozen or more convoluted directories this really is a lifesaver. 

You can see how fish interprets the `abbr` command to create the abbreviation by typing `abbr -s`

```fish
abbr -a -- itchdir 'cd /home/kk/.config/itch/apps/'
```
You can use this fully expanded command style if you prefer.

Addtitionally, you can use `abbr -e` to remove an abbreviation, or `abbr -r` to rename an existing abbreviation (eg `abbr -r itchdir itchd`). The rename feature is quite nice since you can set and forget lengthy commands and paths, and rename them if they become inconvenient without having to set them up again.

Lastly, if you have access to 20th century technological innovations like a Graphical Processing Unit, you can view, add, edit, and delete your fish abbreviations by using fish's built-in `fish_config`.

Feel free to ping with your suggestions, fork, submit a pull request, or hurl insults at me.

Please see the [the official documentation](https://fishshell.com/docs/current/cmds/abbr.html) for more information.
