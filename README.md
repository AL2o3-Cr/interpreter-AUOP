<meta charset="UTF-8">
<meta lang="RU">

# Интерпретатор-UniJect

Самое важное - это изменение синтаксиса прямо в процессе выполнения программы

```script
Syntax 0
:
&num0..0&num0;ignore
:
```
добавляет синтаксис коментариев
`Syntax 0` - `0` id ситаксиса для обращения к нему в дальнейшем.  
`&num0` - Из html, означает знак `#`. `0` - оканчание фрагмента ситаксиса.  
`..0` - что-либо.  
`;` - оканчивает синтаксис, дальше - что он делает.  
`ignore` - действие синтаксиса - игнориравание участка обрамлёного `#`.



built-in :
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
    !class0&dollar0!name;DeclarateVoid
    name=text0class=DeclaratedObj
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
* Variable :
    * `_GLOBAL` - access to top objects from everywhere
* Meths :
    * `__D(class, name, value);`  
    Declaration new object in 

    * `__S(Var N, obj V);`  
    Change `< V >` of an < name > in current namespace. Arguments add `__S(uj,"foo", {_Args.__D(class, name, {});})` is correct.

    * `__R(Var N);`  
    Remove obj < N > from < name >
    * `ifs(cond{< bool >}, true{< execed object >},\ false{< execed object >});`
    * `while(cond, true,\ );`
    * `foreach(code, count || str || _list, )`

* SubObjects for any object :
    * `_C`  
    class
    * `_N`  
    original name
    * `_P`  
    Parent
    * `_Args`  
    list named/indexed objects from (< arguments >)
    * `_M`  
    list attributes
    * `_L`  
    all local objects