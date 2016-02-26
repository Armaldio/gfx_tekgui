Interactions
===

Now that you know how to design your basic interface, what about interacting with it ?

Interacting with components
---
There are several function to make your life easier
All the function are based on the name of your component.
to refresh a bit your memeory, the name of your component is his ***scope***

Ok, say we have a button like this :
```ini
[btn1]
borderColor=112,112,112
innerColor=212,212,212
borderSize=1
fontSize=1
pos=10,10
size=150,50
text="OK"
fontColor=0,0,0
onclick=click
```

And i want to grab the current state of the button loaded in memory, what should I do ?
I just have the function : `button_get`

Here is how to use it :

```c
t_button  *button;

button = button_get(gui, "btn1")
button->text = "Hello";
```

If you don't want to define a variable, to reduce code size, you can also do it this way :

```code
button_get(gui, "btn1")->text = "Bonjour";
```

Now you can interact with your button and access all it's components
It also works for all the components
I invite you to read the [function list](/en/function_list.md) to know all the capabilities.


Adding new components
---
TODO

User utility
---
It's cool to add custom triggers but how can I get custom values ?
The answer is `userdata` !
in fact, inside the `t_tekgui` structure there is a variable called `userdata` of type `void *`

You don't know how to use it ?
It's easy :

- define a custom structure
```c
typedef struct	s_myuserstructure
{
    char      	*text;
}		         t_myuserstructure;
```

- Put it in your main
```c
//Define structure
t_myuserstructure	st;

//Set data inside structure
st.text = "Bonjour";

//Set userdata equal to your datas
gui->userdata = &st;
```
- Every trigger receive the `t_tekgui` structure
Grab your datas like this :

```c
//Function triggered when a button is clicked
void			click(void *data)
{
  //Define t_tekgui and t_myuserstructure
  t_tekgui		*gui;
  t_myuserstructure	*st;

  //get gui structure from data
  gui = (t_tekgui *) data;

  //get your structure from userdata
  st = (t_myuserstructure *) gui->userdata;

  //Now feel free to use you data as want :)
  my_putstr(st->text);
}
```
