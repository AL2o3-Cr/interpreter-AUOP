<head>
<meta charset="UTF-8">
<meta lang="RU">
<title>UniJect.md</title>
</head>

# Интерпретатор-UniJect

Самое важное - это изменение синтаксиса прямо в процессе выполнения программы

```
Syntax 0
:
&num0..0&num0;ignore
:
```
добавляет синтаксис коментариев  
`Syntax 0`, - `0` id ситаксиса для обращения к нему в дальнейшем.  
`&num0` - Из html, означает знак `#`. `0` - оканчание фрагмента ситаксиса.  
`..0` - что-либо.  
`;` - оканчивает синтаксис, дальше - что он делает.  
`ignore` - действие синтаксиса - игнориравание участка обрамлёного `#`.

Программа на *UniJect* разделена на именые пространства. Любой объект - своя область имен. Но в любой `namespace` встроенны следущие имена:
* `__D(class, name, value);`  
Declaration new object in 

* `__S(Var N, obj V);`  
Change `< V >` of an < name > in current namespace. Arguments add `__S(uj,"foo", {_Args.__D(class, name, {});})` is correct.

* `__R(Var N);`  
Remove obj < N > from < name >
* `_C`  
class
* `_N`  
original name
* `_P`  
Parent
* `_G`  
access to top objects from everywhere
* `_Args`  
list named/indexed objects from (< arguments >)
* `_M`  
list attributes
* `_L`  
all local objects

Встр :
* syntax :
    ```
    Syntax 0
    :
    &num0..0&num0;Ignore
    :
    ```
    ```
    Syntax 1
    :
    !class0&dollar0!name;Declarate
    class=DeclaratedObj,=~name
    name=[8bit]<+11
    :
    ```
    ```
    Syntax 2
    :
    add0 0!module0 %as !name;DeclarateModule
    module=FileName,=FromModules
    name=[8bit]<+2,<+40
    :
    ```
* Classes :
    * `uj` - warp  
    * `var` - string or number for name of arguments
        * `int`
        * `float`
        * `duoble`
        * `str`
        * `bool`  
        . . .
    * `meth` - execution in parent namespace
* func :
    * `ifs(cond{< bool >}, true{< execed object >},\ false{< execed object >});`
    * `while(cond, true,\ );`
    * `foreach(code, count || str || _list, )`