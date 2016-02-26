Construire votre ini
================

Bases
------

Un fichier ini de base est composé d'au minimum :

```ini
[win]
width=500
height=500
name=my_name
bgcolor=240,240,240
```

Mais, qu'est ce que cela veu dire ?

`[win]` indique que nous sommes en train de travailler dans le *__scope__* `win` qui fait référence à la fenêtre principale. Il peut y avoir autant de *__scopes* que vous voulez dans votre fichier ini.

`width`, `height`, `name`, `bgcolor` sont des *__fields__*. Les *__fields__* sont contenus dans les *__scope__*.
Le fihier ini est basé sur un systeme de clé=valeur. La clé est `width` et la valeur `500`.

C'est aussi simple que ça !

Champs supportés
----------------

Il y a beaucoup de champs supportés dans cette librairie. Le fichier ini est concue pour être simple a configurer.

Si vous voulez, par exemple, ajouter un bouton, ajoutez juste un *__scope__*
avec toutes les clés dont un bouton a besoin. Ensuite, ajoutez dans le *__scope__* `win` un champs `buttons` et placez-y les *__scopes__* de votre bouton, séparés par une virgule.
Faîtes bien attention a construire correctememnt votre ini, sinon vous aurez des erreurs.

```ini
[win]
width=500
height=500
name=my_win
bgcolor=240,240,240
buttons=btn1,btn2

[btn1]
borderColor=112,112,112
innerColor=212,212,212
borderSize=1
fontSize=12
pos=10,10
size=150,50
text="OK"
fontColor=0,0,0
textalign=center
onclick=btn1_ok

[btn2]
borderColor=112,112,112
innerColor=212,212,212
borderSize=1
fontSize=12
pos=10,10
size=150,50
text="Cancel"
fontColor=0,0,0
textalign=center
onclick=btn2_cancel
```

Vousci le rendu :

![preview image](http://img15.hostingpics.net/pics/438103sshot2.png)

Maintenant que vous savez comment construire un ini de base, vous devriez lire la section des composants.
Elle liste tous les composants disponibles et leurs clé/valeurs respectives

[Voir les composants](/fr/components.md)
