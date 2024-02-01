# vim fast-cheatsheet
- [basic editing](#basic-editing "goto basic-editing")
- [multi file editing](#multi-file-editing "goto multi-file-editing")
- [vim configuration](#vim-configuration "goto vim-configuration")
# basic editing
- [open save and quit](#open-save-and-quit "goto open-save-and-quit")
- [mode switch](#mode-switch "goto mode-switch")
- [cursor control](#cursor-control "goto cursor-control")
- [folding](#folding "goto folding")
- [contents edit](#contents-edit "goto contents-edit")
- [search and replace](#search-and-replace "goto search-and-replace")
## open save and quit:
```c
        vim /directory/file    /* open file.s */
```
```c
        :w                     /* save file */
        :q                     /* quit */
        :wq                    /* save and quit */
        :q!                    /* quit without save */
```
## mode switch:
- - - -
`Esc` view mode\
`I` inset mode\
`/` search mode\
`:`command mode\
`V`selection mode
- - - -
## cursor control:
- - - -
`H` `J` `K` `L` are ⬅️ ⬆️ ⬇️ ➡️ that every vim user knows
- - - -
- - - -
`W` forword\
`B` backword\
\
`$` tail of line\
`0` mane of line
- - - -
```c
        :255                   /* goto line 255 of file */
```
`Shift` + `G`  goto tail of file\
`G` + `G` goto mane of file
- - - -
## folding:
- - - -
`Z` + `F` manually create a fold from a selection
- - - -
- - - -
`Z` + `A` fold or open automatically\
`Z` + `O` open fold\
`Z` + `C` close fold\
`Z` then `Shift` + `R` open all folds\
`Z` then `Shift` + `M` close all folds
- - - -
## contents edit:
- - - -
`U` undo\
`Ctrl` + `R` redo
- - - -
- - - -
`A` insert after current char\
`Shift` + `A` insert at end
- - - -
`O` insert below current line\
`Shift` + `O` insert above current line
- - - -
- - - -
`X` cut current char or selected chars\
`3` + `X` cut three chars; `4` + `X` cut four chars and so on\
\
`D` + `D` cut current line\
`4` then `D` + `D` cut 4 lines; `5` then `D` + `D` cut 5 lines and so on\
\
`D` + `W` cut forword\
`D` + `B` cut backword\
\
`D` + `$` cut to end\
`D` + `0` cut to home
- - - -
`Y` copy selection\
\
`Y` + `Y` copy current line\
`2` then `Y` + `Y` copy 2 lines\
\
`Y` +`W` copy forword\
`Y` + `B` copy backword\
\
`Y` + `$` copy to end\
`Y` + `0` copy to home\
\
`P` paste
- - - -
## search and replace:
```c
        /mlp-fim               /* search mlp-fim */
```
- - - -
`N` highlight next\
`Shift` + `N` hilghight previous
- - - -
```c
        :%s/a/b/g              /* replace a, b --all */
        :%s/a/b/gc             /* replace a, b --all --interactive-confirm */
```
```c
        :26,37s/a/b/g          /* replace a, b --start=26 --end=37 */
        :21,$s/a/b/g           /* replace a, b --start=21 --end=end */
```
# multi files editing
```c
        vim /directory/file0 /directory/file1 /directory/file2 ... /* open multi files */
```
```c
        :n                     /* switch to next file */
        :N                     /* switch to previous file */
```
```c
        :e /directory/file     /* open another file */
```
```c
        :buffers               /* show all file buffers */
        :buffer 1              /* goto file buffer 1 */
```
# vim configuration
system wide `/etc/vimrc`\
user specific `~/.vimrc`
```c
        :set number             /* show line number */
        :set nowrap             /* do not wrap text */
        :set cursorline         /* show cursor line */
        :set cursorcolumn       /* show cursor column */
        :set foldmethod=indent  /* fold by code indent. other methods: manual, syntax, marker, foldable block, expr */
```
```c
        :set expandtab          /* expand tab to spaces */
        :set tabstop=4          /* now tab width is 4 spaces */
        :set shiftwidth=4       /* now shift width is 4 spaces */
```
```c
        :set incsearch          /* incremental search */
        :set hlsearch           /* hilight search */
```
- - - -
Licence: [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
