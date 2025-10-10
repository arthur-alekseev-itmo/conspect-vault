### GLB - Gretest Lower Bound.
![[Pasted image 20251010144332.png]]
```fsharp
Having 
a <: super1 <: super2; 
b <: super3; 
b <: super2;

glb(a, b) -> bot
glb(super1, super3) -> bot
glb(super1, super2) -> b
glb(super2, a) -> a

(* Unify function args *)
let f (g : 'a -> 'b -> 'c) (h : 'd -> 'e -> 'f) x y =
	if rand () then g x y else h x y
(* x: glb('a, 'd); y:  glb('b, 'e) *)
(* 'a = super2;  'd = super3 =>  x: b *)
```


### LUB - Least Upper Bound.
![[Pasted image 20251010144947.png]]
```fsharp
Having 
a <: super1 <: super2; 
b <: super3; 
b <: super2;

lub(a, b) -> super2
lub(super1, super3) -> any
lub(super1, super2) -> any
lub(super2, a) -> super2

(* Function return or if else*)
let f () = if rand() then x: a else y: b (* f : unit -> super2 *)
```

### Covariance
```haskell
(a -> b) -> (F a -> F b)
```
For Types
```fsharp
a <: b => F<a> <: F<b>

(* Works for readonly collections *)
IEnumerable<Cat>  <:  IEnumerable<Animal>
```

### Invariance
For Types
```fsharp
a <: b => F<a> </: F<b> && F<b> </: F<a>

(* The strictest and safest *)
```

### Contravariance
```haskell
(a -> b) -> (F b -> F a)
```
For Types
```fsharp
a <: b => F<b> <: F<a>

(* Works for writeonly collections or actions *)
Action<Animal>  <:  Action<Cat>
```