# git notes

## git conf
- adding this to the git conf will mean no more --upstream flags for new branches
    - `git config --global push.autoSetupRemote true`

## add ssh key for github
- `ssh-keygen -c __YourEmail_`
- `cat ~/.ssh/id_......pub` (should have your email in it)

- copy the line that is output
- on github add authentication key (from settings)

