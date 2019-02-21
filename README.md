.chst
======

__What .chst is?__
 * ProgProgrammable cheatsheets/cheatfiles model defintion that can used both  for key combinations or typing.
 * Applications cheatsheets/cheatfiles with default keybindings or commands


.chst how to use:
-----------------
(Step 1)
It is recomended to clone ( or fork and then clone if you plan to have some own customization)  this repo into your ```~/``` directory, or maintain as part of your ```dotfiles```.

e.g
[rchst](https://github.com/hicolour/rchst) primary will search for cheatsheets/cheatfiles in ```~/.pchst``` &  ```~/.chst``` direcotries, and will prioritize the files from  ```~/.pchst``` - personal chst, the one you may not want to share with whole world.

(Step 2)
It is recomended to use [rchst](https://github.com/hicolour/rchst)application as .chst browser ([rchst](https://github.com/hicolour/rchst) is just tiny [rofi](https://github.com/DaveDavenport/rofi) extension)

.chst about itself:
-----------------

PDF or HTML cheatsheets are not very usable and therfe is strong need for interactive easly searchable cheatsheets.
As simple as possible, text based cheatsheets are the fundamenetal building block of final solution.

Key priciples:
 - Single line & simple command
 - Single line, simple & easy searchable intuitive description

This is not inteded to be few-lines per command, or documenetation style formart.

.chst format/model was orginaly designed mainly for [rofi](https://github.com/DaveDavenport/rofi) - a window switcher & application launcher  , simply more advanced dmenu -  and its extension [rchst](https://github.com/hicolour/rchst).

Format is more or less generic and can be used by any type of software that will be able to cosume it as a source of commands or key combinanations cheatsheets.

.chst alternatives
-----------------

Documenenation browsing
- [zeal](https://github.com/zealdocs/zeal)


File format and its versions
--------

| File format version              | Format Defintion                                                           |
| -------------------------------- |:-------------------------------------------------------------------------:|
| `0.0.1`                          | ```Category =\|= Subcategory =\|= Command =\|= Description =\|= Action Type```|


Possible on roadmap:
 - Special character e.g. $ that could be used for placeholder for user input (need to verify if it makes sense on daily basis rutine)
 - Action type ```run``` for running application (need to verify if it makes sense on daily basis rutine)



Command & Action Type
-----------------
How ```Comamnd``` are interpreted depends on ```Action Type```  

Currently there are two actions types:

 - ```key``` - inform .chst browser that command should be executed as key press  
 - ```type```- inform .chst browser that command should be executed just by regular letter typing (e.g. in previously focued window/console)
 - ```input+key``` - inform .chst browser that command should be executed as key press, but before that browser should ask user for input parameters defined in command
 - ```input+type``` - inform .chst browser that command should be executed just by regular letter typing, but before that browser should ask user for input parameters defined in command   


If the ```key``` action type is used, command should contains key combination that is based on the X Keysym strings e.g.
S

```
Super_l+n

```




If the ```type``` action type is used, command can conatins any text e.g.
```
git status
```






Current list of .chst
----------------------

- [git](git) -  Git default commands
- [xmonad](xmonad) - Xmonad Default key bindings



Examples of .chst
----------------------
```type``` command example (git - version controll system):

```
git =|= basics =|= git init                    =|= Initialize a repository          =|= type
git =|= basics =|= git status                  =|= Show status of working tree      =|= type
git =|= basics =|= git add file.txt             =|= Start tracking file.txt           =|= type
git =|= basics =|= git add main.txt            =|= Stage modified file main.txtt      =|= type
```

```key``` command example (xmonad - tiling windows manager):

```
xmonad =|= System =|= Super_L+q                =|= Restart XMonad                    =|= key
xmonad =|= System =|= Super_L+ctrl+q           =|= Rebuild & restart XMonad          =|= key
xmonad =|= System =|= Super_L+shift+q          =|= Quit XMonad                       =|= key
xmonad =|= System =|= Super_L+x                =|= Lock screen                       =|= key
```
