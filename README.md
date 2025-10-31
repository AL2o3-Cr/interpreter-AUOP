# interpreter-AUOP
AUOP - Absolutly Universal Objects Programming. File extension .UO

Basic syntax :

Declaration object  
`< class > < name >(< arguments >){< value >};`

Execution < value > with < input args >  
`(< needed args >,\ < optional/indefinitely named args >){< value >}(< input args >);`

For declarated object  
`< name >(< args >);`

SubObjects for any object :

* `StaticObj __C {< class >};`

* `StaticObj __N {< original name >};`

* `StaticObj __P {< Parent >};`

* `StaticObj __Arg {< list named/indexed objects from (< arguments >) >};`

* `StaticObj __L { get all local objects from < name > };`  
\^ ReadOnly \^

* `meth __S(obj C, Var N, obj V, \ List Args)`  
`{declaration <C> <N>(<Args>){<V>} in the parent object of the method. If it's already in < N >, then change < V >};`

* `meth __D(Var N){ delete obj < N > from < name > };`

built-in :

* Classes :
    * `obj` - warp  
    * `var` - sting or number for name of arguments
        * `int`
        * `float`
        * `duoble`
        * `str`
        * `bool`  
        . . .
    * `meth` - execution in parent namespace
* Variable :
    * `_GLOBAL` - access to top objects from everywhere
* Meth :
    * `ifs(cond{< bool >}, true{< execed object >},\ false{< execed object >});`
    * `while(cond, true,\ );`
    * `foreach(code, count || str || _list, )`