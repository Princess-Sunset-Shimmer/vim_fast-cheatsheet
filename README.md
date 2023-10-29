# vim fast-cheatsheet
[open save and quit](#open-save-and-quit "goto open-save-and-quit")\
[mode switch](#mode-switch "goto mode-switch")\
[cursor control](#cursor-control "goto cursor-control")\
[contents edit](#contents-edit "goto contents-edit")\
[search and replace](#search-and-replace "goto search-and-replace")

## open save and quit:
```c
        vim file.s             /* open file.s */
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
        $                      /* end */
        0                      /* home */
```
```c
        shift + g              /* tail of file */
        g + g                  /* mane of file */
```
## contents edit:
```c
        u                      /* undo */
        ctrl + r               /* redo */
```
```c
        a                      /* insert after current char */
        shift + a              /* insert at end */

        o                      /* insert below current line */
        shift + o              /* insert above current line */
```
```c
        x                      /* cut current char or selecte chars */
        3x                     /* cut three chars, 4x cut for chars and so on */

        dd                     /* cut current line */
        4dd                    /* cut 4 lines, 5dd cut 5 lines and so on */

        dw                     /* cut forword */
        db                     /* cut backword */

        d$                     /* cut to end */
        d0                     /* cut to home */
```
```c
        y                      /* copy selected chars */

        yy                     /* copy current line */
        2yy                    /* copy 2 lines */

        yw                     /* copy forword */
        yb                     /* copy backword */

        y$                     /* copy to end */
        y0                     /* copy to home */

        p                      /* paste */
```
## search and replace:
