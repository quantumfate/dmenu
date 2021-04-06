# The preview of my patched dmenu

![alt text](https://github.com/quantumfate/dmenu/blob/ce90e082aa23a25a827b382c5ceeb3998ae37a98/dmenu.png?raw=true)

# Installation
```
$ git clone https://github.com/quantumfate/dmenu.git
$ cd into directory
$ sudo make install
```
# Usage
```
$ dmenu_run or dmenu_run_history
```
dmenu_run_history will use a script to preselect your recently launched applications

I personally run
```bash
$ dmenu_run_history -i -z 2555 -h 23 -x 0 -y 0 -hp brave,discord,spotify,gyazo,anki -hb "#5A4785" -hf "#dbceea"
```
to make my dmenu look like in the image above.

## Patches that are already applied

### dmenu-xyw-5.0.diff
Allows you to control position and size of dmenu.
Adds -z for length and -x -y for position as an option.
If -b is passed -x and -y will be computed from the bottom.

### dmenu-border-4.9.diff
Adds a border to dmenu.

### dmenu-lineheight-5.0.diff
Adds a -h option that allows you to controll lineheight.

### dmenu-highlight-4.9.diff
Highlights input in search results.

### dmenu-highpriority-4.9.diff
Adds -hp <itemlist> as an option for dmenu. Seperate itemlis with comma. 
It also adds -hb (Background color) and and -hf (Foreground color) as an option.
It Expects HTML Color names or groups as an argument. You can also pass hex in quotations.

# Adjustments
Color scheme and other parameters can be adjusted in config.h.

Refer to https://tools.suckless.org/dmenu/patches/ if you wish to apply more patches.

Place the desired .diff in the dmenu directory and run. 
```
$ patch -p1 < <patch>.diff
```
Keep in mind tho the more patches you apply the more likely it is going to happen that you have to add the lines manually.

When you're done run
```
$ sudo make install
```



