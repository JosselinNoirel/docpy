# Condition booléenne

Une condition booléenne permet de poser une question à l'ordinateur et d'obtenir une réponse sous la forme binaire d'un booléen `True` ou `False`. Par exemple `x > 0` se comprend comme « est-il vrai que ce que contient la variable \(x\) — un nombre sans doute — est strictement supérieur à \(0\) ? »

## Comparaisons numériques

* `a < b`
* `a <= b` pour \(a \leq b\)
* `a == b` égalité
* `a != b` pour \(a \neq b\)
* `a >= b` pour \(a \geq b\)
* `a > b`

Noter que pour l'égalité entre deux nombres flottants, les problèmes liés à la représentation des nombres et aux erreurs de calculs font qu'il n'est pas judicieux de procéder à la comparaison via `a == b`. On préférera quelque chose du genre `abs(a - b) < tol` ou `np.abs(a - b) < tol` où la valeur `tol` pourra valoir quelque chose comme $10^{-10}$. NumPy dispose également d'une fonction `isclose()`.

## Autres conditions

* `a in L` \(a\) fait-il partie de la liste ou du tableau \(L\)
* `opt is None`  tester si une variable contient la valeur spéciale `None`

## Opérations sur les booléens

On peut combiner et modifier des conditions à l'aide d'opérations logiques `and`, `or` et `not`. Par exemple, `x > 0 and y > 0`.
