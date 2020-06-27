# Bash Scripts

These are some simple bash scripts I created for personal use.

## Scripts

### gitdo / gitdop
Usage: `gitdo <commit message>`
It's a simple script of git commands I use in order often. The script shows the results of git diff, and if input 'y' is given, it does `git add .` and commits with <commit message>. If you used gitdop it also pushes to the current branch (HEAD).

## My setup
I prefer to store these in the `~/bin` directory. I have it added to path in `.bashrc`. Then I create symbolic links to the scripts.

```bash
# in ~/.bashrc
export PATH="$PATH:~/bin"

$ cd ~
$ mkdir bin
$ ln -s ${repo_location}/play ~/bin/play
```
You might want to make the scripts executable first.
`$ chmod u+x {script}`

