Welcome to the tutorial of LibTekGui
====================================

Setup
-----

First, create a folder `lib` at the root of your project if it doesn't exist and put the file `libtekgui.a` inside.

Now, you have to edit you Makefile :

Add `LIB_TEKGUI = -Llib -ltekgui` in your variables section and `$(LIB_TEKGUI)` in your compilation line If you don't use Makefile, run cc/gcc command with `-Llib -ltekgui` at the end.

That's all !

Minimum code
------------

You need at least a `main.c` and a `configuration.ini` file.

### Main file

Here is an example of a basic `main.c` file :

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

`t_tekgui` is a structure that contains all the required datas.

To set this var, you have to use `tekgui_load` and pass a configuration file as parameter.

`tekgui_display` is used to put all the data of the `gui` to a `pixelarray` [^1]. There is already a predefined *pixelarray* [^1] inside `t_tekgui`

And finally, `tekgui_show` display a window with all the content of `gui` and `gui->pix`

### Configuration file

Here is an example of a basic `configuration.ini` file :

```ini
[win]
width=500
height=500
name=my_name
bgcolor=240,240,240
```

This file will show an empty window of size `500`x`500`, with the name `my_name` and with the background color `240`,`240`,`240` that is a light grey as the Windows's window background.

A preview with the current settings :

![preview image](http://img15.hostingpics.net/pics/524228myname001.png)

You can now go to the second part to learn how to [Build an ini file](/en/building_ini.md)

[^1]: A pixelarray is a an array of pixels that contains color data.
