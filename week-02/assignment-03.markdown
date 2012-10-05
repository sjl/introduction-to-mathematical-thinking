Assignment 2
============

Problems
--------

### Problem 1

1. `T ⇒ (D ∧ Y)`
2. `T ⇒ (Y ⇒ ¬D)`
3. `T ∧ (T ⇒ ((D ∧ Y) ∨ (¬D ∧ ¬Y)))`

### Problem 2

    φ   ¬φ   ψ   (φ ⇒ ψ)   (¬φ ∨ ψ)
    -------------------------------
    T    F   T   T         T
    T    F   F   F         F
    F    T   T   T         T
    F    T   F   T         T

### Problem 3

That `φ ⇒ ψ` and `¬φ ∨ ψ` are logically equivalent.

This makes sense, because the implication is always true if φ is false.
Otherwise it's only true when ψ is true.  Which is exactly what `¬φ ∨ ψ` says.

### Problem 4

    φ   ψ   ¬ψ    (φ ⇒ ψ)   (φ ⇏ ψ)   (φ ∧ ¬ψ)
    ------------------------------------------
    T   T   F     T         F         F
    T   F   T     F         T         T
    F   T   F     T         F         F
    F   F   T     T         F         F

### Problem 5

That `(φ ⇏ ψ)` and `(φ ∧ ¬ψ)` are logically equivalent.

This makes sense, because the only way for φ to "not imply" ψ is for φ to be
true but ψ be false, which is exactly what `(φ ∧ ¬ψ)` says.
