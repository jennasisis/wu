## wu
a neat wannabe low-level programming language

---

### features

#### currently

- transpilation to lua

- function variants

- type safety

- powerful

- being the language of the future

#### in the future

- partial application, currying

- an interpreter

---

### version 0.0.1

bindings
```
foo := .1234               -- inferred variable
bar: string = "swordfight" -- explicit variable
baz :: true                -- inferred constant
```

block-expression
```
-- just a local scope
{
 foo := 100
 bar :: foo + 100
 
 print(foo, bar)
}

-- blocks return implicitly returns
-- their last value ..
foo :: {
 baz :: (a float) float -> a^10
 baz(100)
}

bar: bool = {
 return true -- "return" = wrong grrrr
}
```

types
```
int float boolean string
```

functions
```
-- functions also implicitly return
add_5 :: (a int) int -> a + 5

apply :: (fun (int) int, a int) -> fun(a)

ten: int = apply(add_5, 15)

-- or not
sub_5 :: (a int) int -> return a - 5
sub_0 :: (a int) int -> {
 return a - 0 -- "return" = sure
}
```

```
-- btw. pipe operators(can only one argument(currently))
fifteen := 10 |> add_5
fifteen := add_5 <| 10
```

function-type
`(type*) type*` e.g. `(int, int) int`(taking two ints, returning int)

```
sub: (int, int) int = (a int, b int) int -> a - b
```

---

### inspiration

- the thing about transpiling to lua, from moonscript

- the weird argument type order, from go

- the lack of inconsistency, not from javascript

- ~~function calls and~~ *the* operators, from haskell/elm etc.

- low-level feel and control, from kai/rust
