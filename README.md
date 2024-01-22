# vim fast-cheatsheet
- [basic editing](#basic-editing "goto basic-editing")
- [multi file editing](#multi-file-editing "goto multi-file-editing")
- [vim configuration](#vim-configuration "goto vim-configuration")
# basic editing
- [open save and quit](#open-save-and-quit "goto open-save-and-quit")
- [mode switch](#mode-switch "goto mode-switch")
- [cursor control](#cursor-control "goto cursor-control")
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
```c
        esc                    /* view mode */
        i                      /* inset mode */
        /                      /* search mode */
        :                      /* command mode */
        v                      /* selection mode */
```
## cursor control:
```c
        h, j, k, l             /* ⬅️, ⬆️, ⬇️, ➡️ that every vim user knows */
```
```c
        w                      /* forword */
        b                      /* backword */
```
```c
        $                      /* tail of line */
        0                      /* mane of line */
```
```c
        :255                   /* the line 255 of file */
        shift + g              /* tail of file */
        gg                     /* mane of file */
```
## contents edit:
```c
        u                      /* undo */
        ctrl + r               /* redo */
```
- - - -
```c
        a                      /* insert after current char */
        shift + a              /* insert at end */
```
```c
        o                      /* insert below current line */
        shift + o              /* insert above current line */
```
- - - -
```c
        x                      /* cut current char or selecte chars */
        3x                     /* cut three chars, 4x cut for chars and so on */
```
```c
        dd                     /* cut current line */
        4dd                    /* cut 4 lines, 5dd cut 5 lines and so on */
```
```c
        dw                     /* cut forword */
        db                     /* cut backword */
```
```c
        d$                     /* cut to end */
        d0                     /* cut to home */
```
- - - -
```c
        y                      /* copy selected chars */
```
```c
        yy                     /* copy current line */
        2yy                    /* copy 2 lines */
```
```c
        yw                     /* copy forword */
        yb                     /* copy backword */
```
```c
        y$                     /* copy to end */
        y0                     /* copy to home */
```
```c
        p                      /* paste */
```
## search and replace:
```c
        /mlp-fim               /* search mlp-fim */
```
```c
        n                      /* highlight next */
        shift + n              /* hilghight previous */
```
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
        :buffers               /* show all opened files in buffers */
        :buffer 1              /* goto file of buffer 1 */
```
# vim configuration
system wide `/etc/vimrc`\
user specific `~/.vimrc`
- - - -
Licence: [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
