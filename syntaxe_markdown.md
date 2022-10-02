# Syntaxe Markdown

## Formatter du texte

La syntaxe Markdown est un langage de formattage de texte. L'essentiel du texte peut être rédigé normalement.

```md
La syntaxe Markdown est un langage de formattage de texte.
L'essentiel du texte peut être rédigé normalement.
```

Noter que les fins de ligne sont converties en espaces mais qu'une ligne blanche (c'est-à-dire deux sauts de ligne consécutifs) signale une fin de paragraphe.

Il est toujours possible de recourir à une syntaxe HTML pour des cas de figure complexes.

Pour les entêtes de chapitre, section, sous-section, utiliser

```md
# Chapitre
## Section
### Sous-section
```

Pour changer de police, on notera

```md
*Italique*
**Gras**
```

Pour donner des listes

```md
Liste non numérotée
* Élément
* Élément
Liste numérotée
1. Élément
2. Élément
```

## Formules mathématiques

Markdown permet d'entrer assez facilement des formules mathématiques assez élaborées grâce à la syntaxe LaTeX. (NB : On prononce habituellement [latek] en français.)

### Intégration de formules

<strong>Formules en ligne</strong> (*inline formulae*) Les formules LaTeX peuvent être intégrées dans un paragraphe `$...$` comme c'est le cas dans ce paragraphe-ci avec le théorème de Pythagore $a^2 + b^2 = c^2$.

```md
Les formules LaTeX peuvent être intégrées dans un paragraphe
`$...$` comme c'est le cas dans ce paragraphe-ci avec
le théorème de Pythagore $a^2 + b^2 = c^2$
```

<strong>Formules centrées</strong> (*display formulae*) Les formules LaTeX peuvent également être présentées sur une ligne à part lorsqu'elles sont importantes
$$
    e^{i\pi} + 1 = 0
$$
ou lorsqu'elles prendraient trop de place à l'intérieur d'un paragraphe.

```md
Les formules LaTeX peuvent également être présentées
sur une ligne à part lorsqu'elles sont importantes
$$
    e^{i\pi} + 1 = 0
$$
ou lorsqu'elles prendraient trop de place à l'intérieur
d'un paragraphe.
```

### Mode mathématique

À l'intérieur des formules, on passe en *mode mathématique*. Cela a pour conséquence que la plupart des espaces sont ignorées. Ainsi `$a+b$` et `$a + b$` produisent le même résultat; idem pour `$(a, b)$` et `$(a,b)$`. Markdown fait appel à un outil nommé MathJax pour produire une formule de bonne facture typographique : les variables sont en italique, les fonctions sont en police droite, un espacement convenable entourent les opérateurs $+$ ou $\cdot$, les relations mathématiques $=$ ou $\leq$.

En mode mathématique, le tiret `-` est compris comme le signe moins $-$ (deux caractères différents).

Les virgules également sont soumises à un espacement particulier pour l'écriture de vecteurs `$(a,b,c)$` produisant ainsi $(a, b, c)$. Cet espacement devient problématique dans les langues qui, comme le français, ont pour séparateur décimal la virgule, car `3,1415` donne $3,1415$ en mode mathématique, car cela est compris comme la juxtaposition de deux entiers, $3$ et $1415$. Deux solutions :

1. utiliser le séparateur décimal anglo-saxon `3.1415` pour $3.1415$ ou
2. entourer la virgule d'accolades `3{,}1415` pour $3{,}1415$.

La première solution, l'utilisation du séparateur `.`, a la préférence de l'équipe pédagogique car elle est cohérente avec la notation qui sera celle des cellules de code. (On évitera d'utiliser la virgule pour séparer les milliers.)

### Indices et exposants

Pour obtenir un indice $x_{10}$ on écrit `x_{10}`.

Pour obtenir un exposant $10^{-4}$ on écrit `10^{-4}`.

### Opérateurs utiles

Les opérateurs de l'addition, de la soustraction et de la division sont simplement `+`, `-` et `/`. Pour la multiplication, vous avez le choix entre (1) ne pas introduire d'opérateur $a b$ avec `a b`, (2) l'opérateur $a\times b$ avec `a \times b` et (3) l'opérateur $a\cdot b$ avec `a \cdot b`.

Pour la division on écrira généralement $a/b$ simplement avec l'opérateur slash $/$. Les fractions, peuvent être obtenues avec `\frac{num}{denom}`
$$
    \frac{f(x + h) - f(x)}{h}
$$

Les opérateurs de comparaisons
`a \leq b` ($a \leq b$)
`a < b` ($a < b$)
`a = b` ($a = b$)
`a > b` ($a > b$)
`a \geq b` ($a \geq b$).

### Lettres grecques et autres symboles

`\alpha`,
`\beta`,
`\gamma`,
`\Gamma`,
`\rho`,
`\sigma`,
`\delta`,
`\Delta`,
`\epsilon`
pour obtenir
$\alpha$,
$\beta$,
$\gamma$,
$\Gamma$,
$\rho$,
$\sigma$,
$\delta$,
$\Delta$,
$\epsilon$, etc.

Autre symbole utile : $\infty$ via `\infty`.

(Cf. [Mathematical expressions](https://www.overleaf.com/learn/latex/List_of_Greek_letters_and_math_symbols) par Overlead.)

### Fonctions mathématiques usuelles

La fonction exponentielle peut utiliser la notation `e^{x}`, `\exp(x)` ou encore (lorsqu'il n'y a pas de méprise possible) `\exp x`. Le logarithme `\log(x)` ou si une autre base est utilisée `\log_{b}(x)`. Les fonctions sinus, cosinus et tangent sont disponibles via `\sin(x)`, `\cos(x)` et `\tan(x)`.

### Commandes diverses

Une somme est obtenue ainsi `\sum_{k = 0}^{+\infty} u_{k}`
pour obtenir
$$
    \sum_{k = 0}^{+\infty} u_{k}
$$

Un produit somme est obtenu ainsi `\prod{k = 0}^{+\infty} u_{k}`
pour obtenir
$$
    \prod_{k = 0}^{+\infty} u_{k}
$$

Une intégrale est obtenue ainsi `\int_{k = 0}^{+\infty} f(x) dx`
$$
    \int_{k = 0}^{+\infty} f(x) dx
$$
