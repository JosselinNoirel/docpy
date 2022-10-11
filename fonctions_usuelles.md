# Fonctions usuelles

## Fonctions Python

Quelques fonctions fondamentales :

* `len(x)` retourne le nombre d'éléments d'une liste Python ou d'un tableau 1D NumPy
* `type(x)` retourne le type d'objet : est-ce un entier, un flottant, une liste, une chaîne de caractères, un booléen, etc. (cf. la page [objets](objet.html))

Python dispose de relativement peu de fonctions mathématiques (outre les opérateurs classiques +, -, *, / et **). Malgré tout, il sera utile dans le cours de connaître :

* `abs(x)` retourne la valeur absolue de \(x\) par exemple dans le calcul d'erreur (il existe une version NumPy `np.abs()` également)

D'autres fonctions mathématiques existent mais ne seront pas d'une grande utilité :

* `divmod(x)` retourne le reste et la division entière en un tuple
* `min(x, y, z,...)` le minimum d'une liste, d'un tableau (aussi `np.min()`)
* `max(x, y, z,...)` le maximum (aussi `np.max()`)
* `round(x)` (aussi `np.round()`)

**NB :** Pour les opérateurs, voir <!-- TODO syntaxe Python. -->

## Importer une bibliothèque

Pour importer une bibliothèque et enrichir Python on utilise le mot clef `import` :

```Python
import numpy
```

Les fonctions de NumPy sont disponibles via le préfixe `numpy.` (on parle d'**espace de nommage**), par exemple `numpy.sqrt()` pour la racine carrée.  Cette écriture se révèle lourde à l'usage et on peut aussi importer une bibliothèque en introduisant un raccourci pour l'**espace de nommage**. Les fonctions de NumPy sont disponibles via le préfixe `np.`, par exemple `np.sqrt()` pour la racine carrée grâce

```Python
import numpy as np
```

C'est la solution adoptée conventionnellement dans ce cours et dans la communauté du calcul scientifique.

---

On peut importer certains objets spécifique de la bibliothèque :

```Python
from numpy import pi, sqrt, exp, log
```

Les fonctions sont directement accessibles sans préfixe, ainsi on appellera `exp()`.
Ces objets peuvent être éventuellement renommés au passage :

```Python
from numpy import pi as π
```

Enfin, on peut choisir en principe d'importer tous les objets mais l'usage résiste à cette solution :

```Python
from sympy import *
```

---

**NB :** La bibliothèque Math, standard, fournit de nombreux équivalents aux fonctions mathématiques de NumPy mais leur utilisation ne s'applique pas à des listes ou des tableaux NumPy et elle n'est que rarement chargée.

## Liste de bibliothèques

Bibliothèques usuelles dans ce cours :

* NumPy `numpy as np`
* Matplotlib `matplotlib.pyplot as plt`

Bibliothèques hors programme :

* Math     pour des fonctions mathématiques
* Autograd pour la différentiation automatique
* SymPy    pour du calcul symbolique

## Fonctions NumPy

NumPy définit des fonctions pour la création, la manipulation de *tableaux* ; en outre, NumPy fournit les fonctions mathématiques les plus souvent utilisées dans ce cours comme l'exponentielle, le logarithme, les fonctions trigonométriques, etc. Les opérateurs pour l'addition, la multiplication, etc., décrits dans la partie sur la [syntaxe Python](syntaxe_Python.html) fonctionnent aussi, terme à terme, avec les tableaux NumPy.

Les fonctions NumPy simplifient également la vie pour la [représentation graphique des fonctions](graphiques.html).

Plus d'informations sur la page dédiée : [Bibliothèque NumPy](numpy.html).

## Fonctions Matplotlib

Matplotlib fournit les fonctions nécessaires à la création de graphiques (fonction [[plot (fonction Matplotlib)|plot]] notamment) et l'annotation de graphiques (text, xlabel, etc.). En conjonction avec NumPy, Matplotlib simplifie la vie pour la [[Graphiques et visualisation|représentation graphique des fonctions]].

Plus d'informations sur la page dédiée : [[Bibliothèque Matplotlib]].
