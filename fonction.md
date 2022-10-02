# Fonctions

Pour le nommage d'une fonction, les mêmes règles que pour une [variable](variable) s'applique.

La syntaxe générale est la suivante :

```
def FUNC(ARG1, ARG2,...):
    BODY
    BODY
    BODY
    return VALUE
```

Avec des indentations pour indiquer l'étendue du bloc des instructions de la fonction.

L'appel d'une fonction donne une valeur qui est substituée dans un calcul. On dit que c'est la valeur retournée par la fonction et cela est signalé dans le corps de la fonction par le mot clef return.

## Définir une fonction mathématique

Pour une fonction mathématique, on peut définir une fonction Python en deux lignes :

```Python
def f(x):
    return np.exp(np.abs(np.sin(x)))
```

où l'on modifie l'expression retournée selon la fonction mathématique à définir. Vous aurez sans doute besoin des fonctions de la bibliothèque NumPy.

**NB :** l'indentation en début de ligne, en amont du return est capitale car elle renseigne Python sur le bloc d'instructions qui constitue le corps de la fonction.

### Quels sont les avantages ?

* Le code est modulaire : on peut rapidement étudier une fonction différente en ne modifiant qu'un seul point du code.
* Le code est plus lisible et plus proche des notations mathématiques.
* Le code est plus concis et cela permet de prévenir les incohérences et les bugs.

## Définir une fonction programmatique

On peut aussi définir une fonction de façon à automatiser une tâche. Par exemple, s'il vous est souvent utile de calculer la somme des éléments positifs d'une liste, on peut définir une telle fonction.

```Python
def sum_pos(x):
    s = 0.
    for xval in x:
        if xval > 0.:
            s = s + xval
    return s

sum_pos([9, -5, -7, 9, -5, -6, -3, 5, -5, 6])
```

La variable \(s\) définie dans le corps de la fonction (délimité par l'indentation) est une variable locale : elle sera invisible en dehors de la fonction.

Le mot clef `return` signale quelle valeur doit être retournée par la fonction, c'est-à-dire la valeur qui est substituée à un appel ultérieur de `sum_pos(...)`.
