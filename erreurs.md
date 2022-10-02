# Erreurs classiques

## Variable non définie

<pre><span style='color: red'>NameError</span>: name 'a' is not defined</pre>

**Explication.** La variable référencée dans le code n'existe pas : Python a beau consulter sa mémoire, aucune variable de ce nom n'existe.

1. Si vous venez d'ouvrir un carnet Jupyter, il est peut-être nécessaire d'exécuter certaines cellules du carnet avant d'en arriver au calcul qui provoque l'erreur.  (Il n'est pas exclu que lors de la création du carnet, la cellule définissant la variable \(a\) ait été insérée par erreur plus bas que celle du calcul provoquant l'erreur.  Il n'est pas non plus exclu que la cellule ayant défini la variable ait été retirée par erreur.)

2. Il est possible que vous exécutiez une cellule de code donnant l'impression de définir la variable \(a\) mais qu'elle soit en fait inopérante. Par exemple, si l'affectation est soumise à une condition que vous pensez *vraie* à tort :

```Python
if b < 0:
    a = 3.1415
```

## Indentation

L'**indentation** en block est importante en Python : elle marque d'un point de vue syntaxique les relations de dépendance des diverses instructions.  Dans l'exemple suivant

```Python
if b < 0
    if a < 0:
        c = a * b
```

l'instruction `c = a * b` est subordonné au deuxième `if`, qui lui-même dépend du premier.

<pre><span style='color: red'>IndentationError</span>: expected an indented block</pre>

<pre><span style='color: red'>IndentationError</span>: unexpected indent</pre>

## Utilisation des listes

### Utilisation des indices pour des objets qui ne sont pas des listes

Il est possible d'accéder à un élément d'une liste via <code>L[i]</code>. Mais si <code>L</code> n'est pas une liste ou un dictionnaire par exemple, les crochets (*subscript* le fait de passer un indice) n'ont pas de sens et leur utilisation fautive produit une erreur telle que

<pre><span style='color: red'>TypeError</span>: 'int' object is not subscriptable</pre>

Le message d'erreur peut aussi parler d'autres objets comme les nombres à virgule :
`'float' object is not subscriptable`, etc.

### Utilisation d'indices trop grands

Si une liste contient 100 éléments, on ne peut ni consulter ni affecter une valeur à l'élément 312. L'indice est en dehors des valeurs possibles.

<pre><span style='color: red'>IndexError</span>: list index out of range</pre>

<pre><span style='color: red'>IndexError</span>: list assignment index out of range</pre>

Pour un tableau NumPy, le même principe s'applique mais les messages d'erreur sont un peu différents

<pre><span style='color: red'>IndexError</span>: index 3 is out of bounds for axis 0 with size 3</pre>

## Erreurs de calcul

### Overflow

Les entiers de Python peuvent en principe être aussi grands que l'on veut (mais la mémoire et le temps de calcul vont tout de même imposer des limites à ce qu'il est possible de faire).  Ce n'est pas le cas des nombres à virgule flottante qui ne peuvent dépasser des nombres de l'ordre de $10^{300}$. Certain calculs dépassant cette valeur génèrent donc une erreur qui peut ressembler

<pre><span style='color: red'>OverflowError</span>: (34, 'Numerical result out of range')</pre>

<pre><span style='color: red'>RuntimeWarning</span>: overflow encountered in exp</pre>

## Erreurs de parenthèses

<!-- TODO -->
