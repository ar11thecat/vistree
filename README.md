# Welcome to vistree!
Vistree is a simple python script that helps visualise the file tree inside a directory.
Basically, if you ever found yourself stuck in a loop of `ls` and `cd` and `ls` again, this is the tool for you.\
_Meant for Linux systems_

## how to install:
Pull the vistree file and move it in `$HOME/.local/bin`.
Then copy and paste this script into your `$HOME/.bashrc` file:
```
# enable scripts in '$HOME/.local/bin/'
export PATH="$HOME/.local/bin:$PATH"
```
Now your ready to go! Just `cd` to your favourite directory and type:
```
vistree -c
```

## usage:
`vistree [-h] [-a] [-c] [path]`

## positional arguments:
`path`:&emsp;directory to visualise

## options:
`-h`, `--help`:&emsp;show this help message and exit.\
`-a`, `--all`:&emsp;show hidden dirs and files: ex. `.git`.\
`-c`, `--compact`:&emsp;reduce sprawl of branchy dirs: compacted files are represented with `... [n]` where n is the number of files not visualised.

## example output:
```
eulerianKmerAssembler/
├── .git/
│   └── ... [11]
├── .gitignore
├── .idea/
│   ├── .gitignore
│   ├── eulerianKmerAssembler.iml
│   ├── inspectionProfiles/
│   │   └── profiles_settings.xml
│   ├── misc.xml
│   ├── modules.xml
│   └── workspace.xml
├── data/
│   ├── aromatase_aa.txt
│   └── aromatase_dna.txt
└── src/
    ├── __pycache__/
    │   └── ... [6]
    ├── alg_utils.py
    ├── decors.py
    ├── main.py
    └── sequence.py
```
