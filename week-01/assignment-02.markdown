Assignment 2
============

Problems
--------

### Problem 1

1. `(π>0)∧(π<10)`: `0 < π < 10`
2. `(p≥7)∧(p<12)`: `7 ≤ p < 12`
3. `(x>5)∧(x<7)`: `5 < x < 7`
4. `(x<4)∧(x<6)`: `x < 4`
5. `(y<4)∧(y^2<9)`: `-3 < y < 3`
6. `(x≥0)∧(x≤0)`: `x = 0`

### Problem 2

1. π is greater than 0 and less than 10.
2. p is greater than or equal to 7, but less than 12.
3. x is greater than 5 but less than 7.
4. x is less than 4.  The `(x<6)` clause is unneeded because anything less than
   4 is also less than 6.
5. y is greater than -3 but less than 3.  This requirement comes from the `(y^2
   < 9)` clause.  Anything larger than 3^2 is larger than 9.  Anything smaller
   than -3^2 is also larger than 9.  The `(y < 4)` clause is irrelevant, because
   we already know y must be less than 3.
6. x equals zero.  This is the only possible number that can satisfy both
   conditions at once.

### Problem 3

If φ1 through φn are related in some way, start by proving the base case and
then prove by induction that φ necessarily implies φn+1.

If they're not related (I'm not sure exactly what this question is asking) then
you have to just prove them all.  I'd start with the one that looked most likely
to be false since if it *does* turn out to be false I can do a lot less work.

### Problem 4

Similar to problem 4: start with the piece most likely to be false, which will
let you short-circuit quickly.

### Problem 5

1. `(π>3)∨(π>10)`: `(π > 3) ∨ (π > 10)`
2. `(x<0)∨(x>0)`: `x ≠ 0`
3. `(x=0)∨(x>0)`: `x ≥ 0`
4. `(x>0)∨(x≥0)`: `x ≥ 0`
5. `(x>3)∨(x^2>9)`: `(x > 3) ∨ (x < -3) ∨ (x > 3)`: `(x < -3) ∨ (x > 3)`

### Problem 6

1. Either π is greater than 3, or it is greater than 10.
2. x does not equal 0.
3. x is greater than or equal to 0.
4. x is greater than or equal to 0 (the `(x > 0)` clause is redundant here).
5. Either x is less than -3, or it is greater than 3.

### Problem 7

Attempt to show one of the pieces is true, starting with the one most likely to
be true (which will let you short-circuit the rest).

### Problem 8

Attempt to show one of the pieces is true, starting with the one most likely to
be true (which will let you short-circuit the rest).

### Problem 9

1. `¬(π > 3.2)`: `x ≤ 3.2`
2. `¬(x < 0)`: `x ≥ 0`
3. `¬(x^2 > 0)`: `¬((x < 0) ∨ (x > 0))`: `¬(x ≠ 0)`: `x = 0` (assuming we're
   talking about ℝ)
4. `¬(x = 1)`: `x ≠ 1`
5. `¬¬ψ`: `ψ`

### Problem 10

1. x is less than or equal to 3.2.
2. x is greater than or equal to 0.
3. x equals 0.
4. x does not equal 1.
5. ψ is true.

### Problem 11

D = "The dollar is strong"

Y = "The Yuan is strong"

T = "New US-China trade agreement signed"

1. "Dollar and Yuan both strong": `D ∧ Y`.  This one translates pretty easily.
2. "Trade agreement fails on news of weak Dollar": `¬D ∧ ¬T`.  The loses the
   "weak dollar *caused* the failure" aspect of the headline.  Maybe
   `(¬D → ¬T) ∧ ¬D` would be better?
3. "Dollar weak but Yuan strong, following new trade agreement": `T ∧ ¬D ∧ Y`.
   Again, this loses the causation aspect.
4. "Strong Dollar means a weak Yuan": `D → ¬Y`.  If this headline is talking
   about something that is actually the case, and not a hypothetical, then
   `D ∧ (D → ¬Y)` is probably more accurate.
5. "Yuan weak despite new trade agreement, but Dollar remains strong":
   `¬Y ∧ T ∧ D`.  This is hard, because it loses the "despite" part of the
   headline.  I don't think there's a way around that though since there's not
   "we expected" logical operator..
6. "Dollar and Yuan can’t both be strong at same time": `(¬D ∧ ¬Y) ∨ (D ∧ ¬Y)
   ∨ (¬D ∧ Y)` or maybe `¬(D ∧ Y)` or maybe `(D → ¬Y) ∧ (Y → ¬D)`.
7. "If new trade agreement is signed, Dollar and Yuan can’t both remain strong":
   `T → ¬(D ∧ Y)` or `T → ((D → ¬Y) ∧ (Y → ¬D))`.
8. "New trade agreement does not prevent fall in Dollar and Yuan":
   `T ∧ (D ∨ ¬D) ∧ (Y ∨ ¬Y)` or `¬(T → D) ∧ ¬(T → Y)`.  This one is tricky but
   I think that last one is clearest.
9. "US–China trade agreement fails but both currencies remain strong":
   `¬T ∧ (D ∧ Y)`.  This one is pretty simple, but again loses that "it's not
   what we expected" vibe.
10. "New trade agreement will be good for one side, but no one knows which.":
   `(T → D) ∨ (T → Y)`.  The headline is ambiguous, but they probably mean "good
   for one side at the expense of the other", in which case:
   `(T → ((D ∧ ¬Y) ∨ (Y ∧ ¬D)))`.

To Think About
--------------

1. It's all semantics.  In the US "innocent until proven guilty" means that
   until you're proven guilty, you're "innocent".  So in that case yes, `¬guilty
   = innocent`.  But if we're just talking about purely whether they did it or
   not (disregarding courtrooms), then still yes, `¬guilty = innocent` because
   if they didn't do it, they didn't do it.

   The only place where there's ambiguity is when you take meaning 1 of "guilty"
   (proven guilty in a court of law) with meaning 2 of innocent (actually did
   not do the crime) or vice versa.  Sure, when you mix meanings like that it's
   obviously not going to make sense.

2. The problem in this one is this line:

   "In terms of formal negation, ["not displeased"] has the form ¬(¬pleased)..."

   Which makes the assumption that "displeased" is equivalent to `¬pleased`.
   That's invalid (`¬pleased` means "I did not have positive feelings about it"
   while "displeased" means "I feel palpably negative about it").  It entirely
   ignores the third case ("I had no overall feelings at all").

   To actually capture what "not displeased" is trying to say:

       let pleased mean "I had overall positive feelings"
       let displeased mean "I had overall negative feelings"
       let ambivalent mean "I had no overall feelings, positive or negative"

       ¬displeased = pleased ∨ ambivalent



