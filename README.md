# myvcs
version control system

## Layout

- compression: record all characters that are different, record space between each different character
	- linked list: one node for amount of space, pointer to node w/ different characters 
	- hex code/character to separate space and char nodes when written to file?
		- could this be included in the struct itself?
	- put each character/space different in struct, don't group characters/spaces

- base/reference files: (1st commit) will have their directory
- hash/identifier for now: random string generator

## Directory Structure
- base `.rep` folder in directory
	- (loop through `DIR` object instead?) file w/ list of commit hashes/identifiers
	- [x] each commit identifier will be a directory inside `commits`
	- [x] `base` directory will have files from first commit
	- [x] have `.gitignore`-like file
		- identifiers: f - file, ext - extension

## TODO
- make new commits by comparing prev. commit (current function gives persistent malloc error when enabled)
- if there's a malloc error, `make clean` and compile again
- figure out why modified file of different length than original causes malloc failure
