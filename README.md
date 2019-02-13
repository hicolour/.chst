.chts
=======
Applications cheatsheets that can use both key combinations or typing.

.chts about itself:
-----------------

PDF or HTML cheatsheets are not very usable and therfe is strong need for interactive easly searchable cheatsheets.
As simple as possible, text based cheatsheets are the fundamenetal building block of final solution. 

.chts format was orginaly designed mainly for [rofi](https://github.com/DaveDavenport/rofi) - a window switcher & application launcher  , simply more advanced dmenu -  and its extension rofi-chts.

Format is more or less generic and can be used by any type of software that will be able to cosume it as a source of commands or key combinanations cheatsheets.

.chts alternatives
-----------------

Documenenation browsing
- [zeal](https://github.com/zealdocs/zeal)


File format and its versions
--------

| File format version              | Format Defintion                                                           | 
| -------------------------------- |:-------------------------------------------------------------------------:| 
| `0.0.1`                          | ```Category =\|= Subcategory =\|= Command =\|= Description =\|= Action Type```|


Command & Action Type
-----------------
How ```Comamnd``` are interpreted depends on ```Action Type```  

Currently there are two actions types:

 - ```key``` - inform .chts browser that command should be executed as key press  
 - ```type```- inform .chts browser that command should be executed just by regular letter typing (e.g. in previously focued window/console)

If the ```key``` action type is used, command should contains key combination that is based on the X Keysym strings e.g.
```
Super_l+n

```
If the ```type``` action type is used, command can conatins any text e.g.
```
git status
```

Current list of .chts
----------------------

- [git]()
- [xmonad][xmonad]
