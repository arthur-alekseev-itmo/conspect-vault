From deepseek (NEEDS REFERENCES)

|System|Paradigm|Key Idea|Used In|Key Paper(s)|
|---|---|---|---|---|
|**Hindley-Milner**|Functional|Global constraint solving (unification) for parametric polymorphism. Infers the most general type.|OCaml, SML, Haskell (core), Rust (core)|Damas & Milner (Algorithm W)|
|**Bidirectional**|Functional / Mixed|Separates type checking into "type synthesis" (inferring) and "type checking" (verifying). More predictable and extensible.|Scala, Rust (parts), Haskell (GHC), Idris|Dunfield & Krishnaswami|
|**Local Type Inference**|OO / Generic|Infers type arguments for generics and local variables, but relies on declared signatures for methods.|Java (`var`), C# (`var`), C++ (`auto`)|Pierce & Turner|
|**Gradual Typing**|Dynamic/Static Mix|Uses a dynamic type (`?`) and inserts runtime checks at the boundary between static and dynamic parts.|TypeScript, Python (mypy), Racket|Siek & Taha|
|**Semantic Subtyping**|Set-theoretic|Models types as sets of values, allowing powerful combinations with union/intersection/negation types.|TypeScript, CDuce, ReasonML|Castagna & Frisch