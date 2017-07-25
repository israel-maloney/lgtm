# LGTM 
LGTM is a development process script for merging changes to master. 
When you're ready to merge your branch into master, just execute: `lgtm`

[![asciicast](https://asciinema.org/a/JCKueQxZS0qOQSmOUxulHEHyw.png)](https://asciinema.org/a/JCKueQxZS0qOQSmOUxulHEHyw)

# Installation
Just clone the repo and copy the lgtm script somewhere in your path.
For example:
```
git clone https://github.com/israel-maloney/lgtm.git
cp lgtm/lgtm /usr/local/bin
```

# Configuration
By default lgtm merges changes from your branch into a branch named master.
This can be overridden on a repo basis via lgtm's config file `~/.lgtm/config.json`
For example, let's say the we have a repo name rexrepo and pull requests are merged
to a branch named development (rather than master).

Simply add an entry to ~/.lgtm/config.json for mapping rexrepo to development.
```
{
  "rexrepo": "development"
}
```

# Usage
lgtm runs in caution mode by default and will prompt you for confirmation prior
to every command that it executes giving you complete control over the command flow.
In this usage lgtm just serves as training wheels for keeping your merge to master
dead simple and in compliance with the development process.
```
cd <git dir where you are working>
lgtm
```

You can also pass the branch that will be merged on the command line.  This bypasses
the branch selection but still prompts for confirmation prior to executing any command.
```
lgtm my-awsome-branch
```

# Normal mode
Merging to master is a delicate task, as such lgtm runs in caution mode
by default.  To run in normal mode pass the -n flag to lgtm.  In normal mode
lgtm will only prompt you prior to actually pushing changes to the remote master branch.
This workflow can be a bit faster and is still quite safe.
```
lgtm -n
```

