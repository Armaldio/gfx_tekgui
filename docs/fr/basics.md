Bienvenue dans le tutoriel de la LibTekGui
====================================

Installation
-----

Premierement, créez un dossier `lib` à la racine de votre projet si il n'existe pas.
Placez-y ensuite le fichier `libtekgui.a`.

Maintenant il faut éditer votre Makefile

Ajoutez `LIB_TEKGUI = -Llib -ltekgui` dans vos variables et `$(LIB_TEKGUI)` dans votre ligne de compilation.
Si vous n'utilisez pas de makefile, lancez `cc/gcc` avec `-Llib -ltekgui` en arguments.

C'est tout !

Code minimal
------------

Vous avez besoin d'au moins un fichier `main.c` un fichier de configuration : `configuration.ini`.

### Fichier `main`

Voici un exemple basic de `main.c` :

```c
int	main()
{
  t_tekgui		*gui;

   gui = tekgui_load("full.ini");
   gui->pix = bunny_new_pixelarray(gui->size.width, gui->size.height);
   tekgui_display(gui->pix, gui);
   tekgui_show(gui);
   return(0);
}
```

`t_tekgui` est une structure qui contient toutes les données de l'interface.

Pour définir cette variable, vous avez à vote disposition la fonction `tekgui_load`. Vous devez lui passer un fichier de configuration en parametre.

`tekgui_display` est utilisée pour mettre toutes les données de `gui` dans un `pixelarray` [^1]. Il y a déja un `pixelarray` [^1] dans la structure `t_tekgui`

Pour terminer, `tekgui_show` affiche la fenetre avec le contenu de `gui` et `gui->pix`

### Fichier de configuration

Voici un exemple basique de fichier de configuration `configuration.ini` :

```ini
[win]
width=500
height=500
name=my_name
bgcolor=240,240,240
```
Ce fichier générera une fenetre vide de taille `500`x`500`, avec comme nom `my_name` et avec une couleur de fond `240`,`240`,`240` (ce qui corresponds au gris clair similaire aux interfaces Windows).

Une prévisualisation du rendu :

![preview image](http://img15.hostingpics.net/pics/524228myname001.png)

Vous pouvez maintenant vous rendre a la seconde partie pour apprendre comment [construire un fichier de configuration complet](/fr/building_ini.md)

[^1]: Un `pixelarray` est un tableau d'entier non signés qui contient les caractéristiques de chaque pixel (leur couleur).
