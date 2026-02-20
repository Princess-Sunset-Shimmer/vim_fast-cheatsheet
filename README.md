# vim fast-cheatsheet
- [basic editing](#basic-editing "goto basic-editing")
- [multi files](#multi-files "goto multi-files")
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
`Esc` normal mode\
`I` inset mode\
`/` search mode\
`:` command mode\
`V` visual mode\
`Shift` + `R` replace mode
## cursor control:
`H` `J` `K` `L` are ⬅️ ⬆️ ⬇️ ➡️ that every vim user knows\
\
`W` forword\
`B` backword\
\
`Shift` + `$` tail of line\
`0` mane of line
```c
        :255                   /* goto line 255 of file */
```
`Shift` + `G`  goto tail of file\
`G` + `G` goto mane of file
## folding:
`Z` + `F` manually create a fold from a selection\
`Z` + `A` fold or open automatically\
`Z` + `O` open fold\
`Z` + `C` close fold\
`Z` then `Shift` + `R` open all folds\
`Z` then `Shift` + `M` close all folds
## contents edit:
`U` undo\
`Ctrl` + `R` redo\
\
`A` insert after current char\
`Shift` + `A` insert at end\
\
`O` insert below current line\
`Shift` + `O` insert above current line
```c
        :read !SHELL_COMMAND   /* run shell command and insert its output into current file */
```
example: you can use this trick to read long output from a command without save it
```c
        vim
        :read !SHELL_COMMAND --help
        :q!
```
general text editing gramma:
```
        [COUNT] oprator [text_object or motion]
        :[range] command [arguments]
```
`C` + `I` + `W` change inner word\
\
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
```c
        :7,19d                /* cut contents from line 7 to 19 */
        :7,$d                 /* cut dontents from line 7 to bottom */
        :%d                   /* cut all */
```
`Y` copy selection\
\
`Y` + `Y` copy current line\
`2` then `Y` + `Y` copy 2 lines\
\
`Y` +`W` copy forword\
`Y` + `B` copy backword\
\
`Y` + `$` copy to end\
`Y` + `0` copy to home
```c
        :3,9y                 /* copy contents from line 3 to 9 */
        :3,$y                 /* copy contents from line 3 to bottom */
        :%y                   /* copy all */
```
`P` paste\
`3` + `P` paste 3 times
## search and replace:
`Ctrl` + `N` or `Ctrl` + `P` in insert mode, search and auto complete current word
```c
        /mlp-fim               /* search mlp-fim */
```
- - - -
`N` highlight next\
`Shift` + `N` hilghight previous
- - - -
```c
        :%s#a#b#g
        :%s/a/b/g              /* replace a, b --all */
        :%s#a#b#gc
        :%s/a/b/gc             /* replace a, b --all --interactive-confirm */
```
```c
        :26,37s#a#b#g
        :26,37s/a/b/g          /* replace a, b --start=26 --end=37 */
        :21,$s#a#b#g
        :21,$s/a/b/g           /* replace a, b --start=21 --end=end */
```
# multi files
## buffers:
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
## netrw:
```c
        vim /directory          /* open vim and explore specified directory */
        :Ex                     /* explore current directory */
        :Ex /directory          /* explore specified directory */
```
- - - -
`G` + `H` hide or show hidden .files and ./directories\
`S` toggle sort by name, size, time and exten\
\
`-` go previous directory\
`J` and `K` navigate up and down\
\
`Shift` + `R` rename a file\
`Shift` + `D` delete a file\
`D` create a directory\
`Shift` + `%` create a file\
\
`Enter` open file\
`O` open file in new hrizontal split\
`V` open file in new vertical split\
`t` open file in new tab\
\
`Ctrl` + `W` then `H` `J` `K` `L` nevigate between file splits\
`G` + `T` go to next tab\
`G` then `Shift` + `T` go to previous tab
- - - -
# vim configuration
system wide config file: `/etc/vimrc`\
user specific config file: `~/.vimrc`
```c
        :set number             /* show line number */
        :set nowrap             /* do not wrap text */
        :set cursorline         /* show cursor line */
        :set cursorcolumn       /* show cursor column */
        :set foldmethod=indent  /* fold by code indent. other methods: manual, syntax, marker, foldable block, expr */
```
```c
        :set expandtab          /* expand tab to spaces */
        :set tabstop=4          /* now tab width looks like 4 spaces */
        :set softtabstop=4      /* now tab width acts like 4 spaces */
        :set shiftwidth=4       /* now shift width is 4 spaces */
        :set autoindent         /* turn on indent */
        :set smartindent        /* enhance indent */
```
```c
        :set incsearch          /* incremental search */
        :set hlsearch           /* hilight search */
```
- - - -
Licence: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
