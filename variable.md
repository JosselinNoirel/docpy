# Variables

## Affectation

Les variables Python permettent de stocker des informations dans la mémoire de l'ordinateur pour pouvoir les réutiliser et éventuellement les modifier ultérieurement.

On dit que l'on affecte une variable lorsqu'on attribue une valeur à une variable (**affectation**). Cela se fait à l'aide de l'opérateur `=`.

```Python
k = 10
```

**NB :** Il faut bien distinguer l'opérateur `=` de Python qui attribue une valeur à une variable et la relation mathématique \(=\) qui affirme l'identité entre deux objets. Par conséquent, il est possible d'écrire en Python `k = k + 1` (qui modifie la valeur stockée par la variable \(k\) en l'incrémentant d'une unité, \(k\) passerait par exemple de 10 à 11) alors que la relation mathématique \(k = k + 1\) n'a évidemment pas de sens.

Il convient également de distinguer l'opérateur d'affectation `=` et le signe `=` qui intervient dans les arguments nommés des appels de fonction (cf. [syntaxe Python](syntaxe_Python.html)).  Ainsi, dans ce qui suit, il n'est aucunement question de considérer que la valeur $20$ est affectée à une variable `num` :

```Python
linspace(0, 1, num=20)
```

## Comment nommer ses variables

Le nommage des variables est une vraie question. En effet, le plus grand danger dont il faut se prémunir c'est d'affecter une valeur à une variable qui est utilisée par ailleurs dans le programme et que ce conflit engendre des erreurs (ou pire, des bugs silencieux).

Techniquement, une variable commence par une lettre suivie d'une combinaison de lettres, chiffres et underscores. Le principe de nommage est simple : les noms de variable doivent être lisibles, pratiques à taper et faciles à se remémorer.  Il faut éviter les `foo`, `bar` et autres `toto`.

Les noms courts \(m\), \(n\), \(k\), \(x\), \(y\) sont souvent utilisées pour des informations éphémères (par exemple, le compteur d'une boucle). Leur nom est souvent utilisé conventionnellement pour des types d'information particuliers. Ainsi \(m\), \(n\), \(i\), \(j\) ou \(k\) désignent souvent des entiers (naturels ou relatifs).

Des noms courts, comme `dat` (pour des données), ou très courts, comme \(M\), \(S\) (pour des matrices ou des paramètres), peuvent être employés pour des informations pérennes mais utilisées fréquemment : la fréquence de leur utilisation permet de ne pas se poser la question de leur contenu et par ailleurs la facilité d'écriture s'en trouve rapidement rentabilisée.

Des noms plus longs, comme `net_sparsity`, gagnent à expliciter des informations pérennes mais utilisées très ponctuellement. (Techn)

On peut utiliser pour certains paramètres des lettres grecques comme \(\alpha\), \(\Delta\), etc. Pour ce faire, il suffit d'utiliser UTF-8 ou de recourir à un raccourci de Jupyter qui consiste à taper le code LaTeX pour la lettre (par exemple `\Delta`) puis presser la touche TAB. (Cf. [Mathematical expressions](https://www.overleaf.com/learn/latex/List_of_Greek_letters_and_math_symbols) par Overlead.) Ces caractères non latins peuvent être mélangés à d'autres lettres \(\Delta x\) constituant par exemple un nombre de variable valide.

## Variables globales, variables locales

<!-- TODO -->
