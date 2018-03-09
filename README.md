# Useful Linux commands

__Last modified files__
```
find $1 -type f -print0 | xargs -0 stat --format '%Y :%y %n' | sort -nr | cut -d: -f2- | head
```
__Find a string inside files__
```
grep -rnw '/path/to/somewhere/' -e 'pattern'
grep --include=\*.{extensionfile1,extensionfile2} -rnw '/path/to/somewhere/' -e "pattern"
grep --exclude=*.extensionfile1 -rnw '/path/to/somewhere/' -e "pattern"
grep --exclude-dir={dir1,dir2} -rnw '/path/to/somewhere/' -e "pattern"
```
