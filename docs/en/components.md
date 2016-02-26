Data types
==========

Color
-----

A color is a set of 3 values, between 0 and 255, separated by commas. <br> ex: `26,22,128` <br> The color is ![preview image](/img/blue_color.png)

Position
--------

A position is a set of 2 values, separated by comas <br> ex: `50,100` <br> This position is relative to the window

Size
----

A size is a set of 2 values, separated by comas <br> ex: `16,16` <br> This position is relative to the window

String
------

A string is a list of char <br> ex: `"Hello"` <br> A string is always between double quotes " "

Function name
----

A Function name is a string that correspond to a function inside your code <br> ex: `tekgui_load`

Components
==========

Window
-------

Inside your `win` ***scope*** :

`width` require a integer

`height` require a integer

`name` require a [string](/en/components/#string)

Button
-------

![preview](/img/button.png)

Inside `win` ***scope*** :

```ini
buttons=btn1,btn2

[btn1]
...
```

Inside your button ***scope*** :

`borderColor` require a [color](/en/components/#color)

`innerColor` require a [color](/en/components/#color)

`borderSize` require integer (size in pixels)

`pos` require a [position](/en/components/#position)

`size` require a [size](/en/components/#size)

`text` require a [string](/en/components/#string)

`fontColor` require a [color](/en/components/#color)

`onclick` require a [function name](/en/components/#function-name)

Checkbox
-------

![preview](/img/checkbox.png)

Inside `win` ***scope*** :

```ini
checkboxs=checkboxs1,checkboxs2

[checkboxs1]
...
```

Inside your checkbox ***scope*** :

`fontSize` require integer (size in pixels)

`fontColor`  require a [color](/en/components/#color)

`pos` require a [position](/en/components/#position)

`size` require a [size](/en/components/#size)

`text` require a [string](/en/components/#string)

`oncheckstatechanged` require a [function name](/en/components/#function-name)

Image
-------

Inside `win` ***scope*** :

```ini
images=img1

[img1]
...
```

Inside your image ***scope*** :

`pos` require a [position](/en/components/#position)

`size` require a [size](/en/components/#size)

`onclick` require a [function name](/en/components/#function-name)

`borderSize` require a integer

`borderColor` require a [color](/en/components/#color)

`src` require a [string](/en/components/#string)

Label
-------

![preview](/img/label.png)

Inside `win` ***scope*** :

```ini
labels=label1,label2

[label1]
...
```

Inside your image ***scope*** :

`pos` require a [position](/en/components/#position)

`fontSize` require a integer

`fontColor` require a [color](/en/components/#color)

`text` require a [string](/en/components/#string)

Progressbar
-------

![preview](/img/progressbar1.png)
![preview](/img/progressbar2.png)

Inside `win` ***scope*** :

```ini
progressbars=pgrsbar

[pgrsbar]
...
```

Inside your progressbar ***scope*** :

`borderColor` require a [color](/en/components/#color)

`borderSize` require a integer

`backColor` require a [color](/en/components/#color)

`barColor` require a [color](/en/components/#color)

`pos` require a [position](/en/components/#position)

`size` require a integer

`value` require a integer

`max, min` require a integer


Textbox
-------

![preview](/img/textbox.png)

Inside `win` ***scope*** :

```ini
textboxs=tb

[tb]
...
```

Inside your textbox ***scope*** :

`borderColor` require a [color](/en/components/#color)

`borderSize` require a integer

`fontColor` require a [color](/en/components/#color)

`fontSize` require a integer

`innerColor` require a [color](/en/components/#color)

`pos` require a [position](/en/components/#position)

`size` require a integer

`placeholder` require a [string](/en/components/#string)

`placeholderColor` require a [color](/en/components/#color)

`ontextentered` require a [function name](/en/components/#function-name)

`onclick` require a [function name](/en/components/#function-name)
