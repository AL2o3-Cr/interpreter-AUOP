# interpreter-UniJect

Basic syntax :

Declaration object  
``

Realise object  
``

Attribute  
``

execute < value > with < input args >  
`(< needed args >,\ < optional/indefinitely named args >){< value >}(< input args >);`

SubObjects for any object :

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

* `_L { get all local objects };`

built-in :

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