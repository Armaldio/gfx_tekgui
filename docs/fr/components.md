Type de données
==========

Couleur
-----

Une couleur est définie par un ensemble de 3 valeurs, comprises entre 0 et 255, séparées par des virgules. <br> ex: `26,22,128` <br> La couleur est ![preview image](/img/blue_color.png)

Position
--------

Une position est définie par un ensemble de 2 valeurs, séparées par des virgules <br> ex: `50,100` <br> TCette position est relative à la fenêtre

Taille
----

Une taille est définie par un ensemble de 2 values, séparées par des virgules <br> ex: `16,16`

Chaîne de caractere
------

Une chaine-de-caractere est une chaîne de caracteres <br> ex: `"Bonjour"` <br> Une chaine-de-caractere est toujours entre guillements " "

Nom de fonction
----

Un nom de fonction est une chaine de caractere qu correspond a une fonction présente a l'intereieur de votre code <br> ex: `tekgui_load`

Composants
==========

Fenêtre
-------

Dans votre *__scope__* `win`

`width` est un entier

`height` est un entier

`name` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

Bouton
-------

![preview](/img/button.png)

Dans votre *__scope__* `win`

```ini
buttons=btn1,btn2

[btn1]
...
```

Dans votre *__scope__* bouton :

`borderColor` est une [couleur](/fr/components/#couleur)

`innerColor` est une [couleur](/fr/components/#couleur)

`borderSize` est un entier (en pixels)

`pos` est un [position](/en/components/#position)

`size` est une [taille](/en/components/#taille)

`text` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

`fontColor` est une [couleur](/fr/components/#couleur)

`onclick` est un [nom de fonction](/en/components/#nom-de-fonction)

Case à cocher
-------

![preview](/img/checkbox.png)

Dans votre *__scope__* `win`

```ini
checkboxs=checkboxs1,checkboxs2

[checkboxs1]
...
```

Dans votre ***scope*** checkbox:

`fontSize` est un entier (en pixels)

`fontColor`  est une [couleur](/fr/components/#couleur)

`pos` est un [position](/en/components/#position)

`size` est une [taille](/en/components/#taille)

`text` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

`oncheckstatechanged` est un [nom de fonction](/en/components/#nom-de-fonction)

Image
-------

Dans votre *__scope__* `win`

```ini
images=img1

[img1]
...
```

Dans votre ***scope*** image :

`pos` est un [position](/en/components/#position)

`size` est une [taille](/en/components/#taille)

`onclick` est un [nom de fonction](/en/components/#nom-de-fonction)

`borderSize` est un entier

`borderColor` est une [couleur](/fr/components/#couleur)

`src` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

Label
-------

![preview](/img/label.png)

Dans votre *__scope__* `win`

```ini
labels=label1,label2

[label1]
...
```

Dans votre scope ***scope*** label :

`pos` est un [position](/en/components/#position)

`fontSize` est un entier

`fontColor` est une [couleur](/fr/components/#couleur)

`text` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

Barre de progression
-------

![preview](/img/progressbar1.png)
![preview](/img/progressbar2.png)

Dans votre *__scope__* `win`

```ini
progressbars=pgrsbar

[pgrsbar]
...
```

Dasn votre ***scope*** progressbar:

`borderColor` est une [couleur](/fr/components/#couleur)

`borderSize` est un entier

`backColor` est une [couleur](/fr/components/#couleur)

`barColor` est une [couleur](/fr/components/#couleur)

`pos` est un [position](/en/components/#position)

`size` est un entier

`value` est un entier

`max, min` est un entier


Boîte de texte
-------

![preview](/img/textbox.png)

Dans votre *__scope__* `win`

```ini
textboxs=tb

[tb]
...
```

Dans votre scope ***scope*** textbox :

`borderColor` est une [couleur](/fr/components/#couleur)

`borderSize` est un entier

`fontColor` est une [couleur](/fr/components/#couleur)

`fontSize` est un entier

`innerColor` est une [couleur](/fr/components/#couleur)

`pos` est un [position](/en/components/#position)

`size` est un entier

`placeholder` est une [chaîne de caractères](/en/components/#chaine-de-caractere)

`placeholderColor` est une [couleur](/fr/components/#couleur)

`ontextentered` est un [nom de fonction](/en/components/#nom-de-fonction)

`onclick` est un [nom de fonction](/en/components/#nom-de-fonction)
