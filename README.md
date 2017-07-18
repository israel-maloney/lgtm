# Overview 
lgtm is a development helper script for merging changes to master. 

When you're ready to merge your branch into master, just execute: `lgtm`

# Installation
```
git clone https://github.com/israel-maloney/lgtm.git
cd lgtm
./install
. ~/.bash_profile
```

# Usage
```
cd <git dir where you are working>
lgtm
```

# Other
The installation adds an environment variable PARANOID to your bash_profile.
This causes lgtm to prompt you before every action.  Once you're convinced lgtm
won't mangle your work flow you can delete 'export PARANOID=yes' from your bash_profile
and execute.
```
unset PARANOID
```
