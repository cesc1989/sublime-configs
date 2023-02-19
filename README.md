# Sublime Text 3 Configuration Files

I was using Sync Settings extension but is no longer maintained so went for this "simple" solution.

## How to use

In the computer where these settings are needed go to the Sublime Text folder.

On a M1 Macbook the folder probably is at:

```bash
$ cd ~/Library/Application\ Support/Sublime\ Text/Packages/User
```

On an Intel Macbook the folder should be:

```bash
cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/User
```

And then run these git commands:

```bash
$ git init
$ git remote add origin git@github.com:cesc1989/sublime-configs.git
$ git fetch
$ git reset --hard origin/main
```

With the last line we instruct git to use only files coming from the remote.

We could omit this and do a manual merge of the current files against the incoming ones.

## About the .gitignore

The `.gitignore` file is setup to ignore everything except custom files.

It's done this way because Sublime or Package Control could add files and we'd be running git commands so often.

When adding a new file, also include it in the `.gitignore` prepended with exclamation mark, i.e

```git
# .gitignore

!new_file.txt
```