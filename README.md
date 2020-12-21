# Bash Scripts

These are some simple bash scripts I created for personal use.

## Scripts

<details>
<summary>gitdo</summary>

Usage: `gitdo [options] <commit message>`

It's a simple script of git commands I use in order often. The script shows the results of git diff, and if input 'y' is given, it does `git add .` and commits with (commit message). If you used gitdop it also pushes to the current branch (HEAD).
A wrapper for frequently used git commands. When run, it shows the results of `git status` and adds, commits, and pushes automatically. Default behaviour can be customized. See `gitdo -h` for in-depth help.
Example:
```bash
# Add and commit all changes
$ gitdo "Commit message here"
# Add and commit without asking for confirmation
$ gitdo -a "Commit message here"
# Add, commit, and push without asking for confirmation
$ gitdo -pa "Commit message here"
# Add, commit, and push to 'upstream' without confirmation
$ gitdo -par upstream "Commit message here"
```

</details>

<details>
<summary>play</summary>

Usage: `play [keyword]`

A root music directory is set in the script. When invoked, the script checks the music directory and tries to find a playlist (.xspf extension) and opens it in vlc. If no playlist is found it checks the Albums folder and finds any album with the given keyword and play those in vlc. If no albums are found, it searches the whole music directory, including song/artist names and adds everything that contains the keyword and plays it in vlc.
</details>

<details>
<summary>svcstat</summary>

Usage: `svcstat [stopall]`

Helps to monitor the status of services, specially when you start/stop them frequently. The services checked by the script are in an array, where you can add new services or remove them easily. When invoked with root permissions and the parameter 'stopall' (i.e `$ svcstat stopall`) all services in the array will be stopped.
</details>

<details>
<summary>copy</summary>

Usage: `copy (source) (destination)`

It just calls rsync. I use this when I want to copy something and see progress as well. As of now, this could have been done easier with an alias.
</details>

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

