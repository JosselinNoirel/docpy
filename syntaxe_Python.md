# Syntaxe Python

Rappel : En gras, on retrouve les mots du [glossaire](glossaire.html).

## Comment Python lit du code

Python lit ligne par ligne et s'attend généralement que chaque ligne lui
présente une instruction compréhensible et complète. Si l'instruction
n'est pas complète, Python peut lire la seconde ligne pour voir si elle
complète la première (par exemple si une parenthèse n'a pas été
refermée).

<!-- TODO mot clef -->

Un `#` (*croisillon* ou *hash sign*) initie sur la ligne un
**commentaire**, c'est-à-dire une portion de code qui n'est pas lue par
l'ordinateur mais peut accueillir une annotation destinée au lecteur.

``` python
x = x + 1 # x gets incremented
```

## Contenu d'un programme

Un programme consiste en une suite d'**instructions**. Parmi des
instructions,

-   on peut trouver des **affectations** de [variable](variable.html),
-   on peut trouver des opérations faisant appel à des **opérateurs**
-   on peut trouver des appels de fonctions,
    -   soit des fonctions prédéfinies (par exemple,
        [`len()`](function_len.html)),
    -   soit des fonctions définies par une bibliothèque (par exemple,
        [`linspace()`](function_linspace.html)),
    -   soit encore des fonctions définies par l'utilisateur (cf.
        [fonctions](fonction.html)),
-   on peut trouver des structures de contrôle
    ([if-then-else](if_then_else.html), boucles [for](for.html) et
    [while](while.html)).

## Opérateurs

Les opérateurs les plus courants sont :

* `x + y` et `x - y` l'addition $x + y$ et la soustraction $x - y$
* `x * y` et `x/y`   l'addition $x + y$ et la division $x/y$
* `x**a`             l'exponentiation $x^a$
* `-x`               l'opposé de $x$
* `n % m`            le reste de la division de $n$ par $m$ et
* `n // m`           la division entière     de $n$ par $m$

**NB 1 :** Il n'y a pas d'opérateur dédié pour la racine $n$-ième mais on se souviendra que
$\sqrt[n]{x}$ correspond à l'exponentiation $x^{1/n}$. Par exemple `x**.1` pour une racine dixìeme.

**NB 2 :** Le fonctionnement de ces opérateurs est généralisé pour pouvoir fonctionner terme à terme avec des tableaux NumPy.

## Appel d'une fonction

Une fonction se caractérise par la présence de parenthèses

``` python
func_name(...)
```

Entre les parenthèses, se trouvent le ou les **arguments** de la
fonction `func_name`. (Il est possible également que la fonction ne
prenne aucun argument, l'appel se faisant donc `func_name()`.)

Les arguments, s'ils sont multiples, sont séparés par une virgule :

``` python
func_name(arg1, arg2, arg3)
```

Chaque argument porte un nom dont on peut prendre connaissance en lisant
la documentation de la fonction (voir commencer consulter la [documentation](aide.html)). Par exemple, la fonction `open()`, qui
permet d'ouvrir des fichiers, accepte ces trois arguments nommé *file*,
*mode* et *buffering*, qui sont autant de paramètres qui contrôlent
comment la fonction remplit sa tâche :

``` python
open(file, mode='r', buffering=-1)
```

Certains arguments sont optionnels : ils peuvent être omis, auquel cas
la fonction prévoit généralement une valeur par défaut. Il en va ainsi,
par exemple, des options `mode` (en l'absence d'information, la valeur
`'r'` est utilisée) et `buffering` (en l'absence d'information, la
valeur $-1$ est utilisée) de la fonction `open()` ou encore de l'option
`retstep` de [`linspace()`](function_linspace.html) :

``` python
linspace(0, 10) # The function will assume a default value False (see doc)
linspace(0, 10, retstep=False) # Same as above
linspace(0, 10, retstep=True)  # This alters the behaviour of linspace()
```

Si l'on nomme les arguments, l'ordre ne compte pas vraiment. Ainsi les
deux appels suivants seront strictement équivalents :

``` python
open('corpus.txt', mode='r', buffering=-1)
open('corpus.txt', buffering=-1, mode='r')
```

Voir aussi : les articles concernant les [fonctions](fonction.html)
définies par l'utilisateur et les [fonctions
usuelles](fonctions_usuelles.html) de Python et des bibliothèques NumPy
et Matplotlib.
