Building you ini
================

Basics
------

A basic ini is at least composed of :

```ini
[win]
width=500
height=500
name=my_name
bgcolor=240,240,240
```

But, what it means ?

`[win]` means that we are working in the *__scope__* `win` which refer to the main window. There can be as many *__scopes* as you want in an ini file.

`width`, `height`, `name`, `bgcolor` are *__fields__*. The *__fields__* are contained inside a *__scope__*. It is based on a key/value system. The key is `width` and the value `500`.

It is as simple as this !

Supported fields
----------------

There are many supported fields in this library. The ini is designed to be simple to setup.

If you want for example to add a button, just add a *__scope__* with all the keys needed by your button. Then add a `buttons` key and add all your buttons scopes followed by coma.
Make sure all your datas a right, else you will get errors.

```ini
[win]
width=500
height=500
name=loooul
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

This render as this :

<!--- TODO loooul -->

![preview image](http://img15.hostingpics.net/pics/438103sshot2.png)

Now that you know how to build your ini, you should read this sections that list all the components and keys required by it

[View all the components](/en/components.md)
