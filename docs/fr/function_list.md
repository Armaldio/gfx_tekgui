Functions
===

```c
t_tekgui	*tekgui_load(const char *file);
```
Load a configuration file `file` inside a `t_tekgui *`

---

```c
void		tekgui_unload(t_tekgui *tekgui);
```
Unload `tekgui` from the memory

---

```c
void		tekgui_display(t_bunny_pixelarray	*pix,
                           t_tekgui		       	*gui);
```
Put the graphical representation of `gui` inside `pix`

---

```c
void		fill_color(t_bunny_pixelarray	*pixelarray,
				        unsigned int		color);
```
Fill completely `pixelarray` wiht the color `color`

---

```c
void			set_max_heap_size(size_t);
```
Set the max ram for the program

---

```c
void			tekpixel(t_bunny_pixelarray	*a,
				 t_bunny_position	*p,
				 t_color		*c);
```
Set the color of a pixel at the position `p`, of color `c` and inside `a`

---

```c
t_bunny_position	new_bunny_position(int x, int y);
```
Create a `t_bunny_position` from `x` and `y`

---

```c
t_size			new_size(int w, int h);
```
Create a `t_size` from  width `w` and height `h`

---

```c
void			tekline(t_bunny_pixelarray	*pix,
				t_bunny_position	*pos,
				t_color			*color);
```
Draw a line inside `pix` from `pos[0]` to `pos[1]` of color `color`

---

```c
int			tekgui_putstring(t_text			text,
					 t_bunny_pixelarray	*pix,
					 t_bunny_pixelarray	*font);
```
Put a string from a `t_text` inside `pix` with the font `font`

---

```c
unsigned int		tekgetpixel(t_bunny_pixelarray	*a,
				    t_bunny_position	*p);
```
return in an `unsigned int` the pixel color at `p` inside `a`

---

```c
t_color			new_color(int r, int g, int b, int a);
```
Create a `t_color` from `r`, `g`, `b` and `a` component

---

```c
t_color			load_ini_color(t_bunny_ini *ini,
				       char *field,
				       char *name);
```
load a `t_color` from `ini` at `field`->`name`

---

```c
void			*tekfunction(const char *funcname);
```
Return a function pointer from a `char *` name

---

```c
int			is_hover(t_bunny_position	*from_pos,
				 t_bunny_position	*pos,
				 t_size			*size);
```

Determine if the position `from_pos` is inside the rectangle `pos-size`

---

```c
int			display_button(t_bunny_pixelarray	*pix,
				       t_button			*button,
				       t_bunny_pixelarray	*font);
```
Update the graphics of `button` inside `pix` with the font `font`

---

```c
t_size			load_ini_size(t_bunny_ini *ini, char *scope);
```

load a `t_size` from a `scope` inside `ini`

---

```c
t_bunny_position	load_ini_position(t_bunny_ini *ini, char *scope);

```
Load a  `t_bunny_position` from `scope` inside `ini`

---

```c
int			display_textbox(t_bunny_pixelarray	*pix,
					t_textbox		*textbox,
					t_bunny_pixelarray	*font);
```
Update the graphics of a `textbox` inside `pix` wiht the `font`

---

```c
void			check_box(t_tekgui *gui, t_checkbox *checkbox);
```
Force checking `checkbox`

---

```c
void			uncheck_box(t_tekgui *gui, t_checkbox *checkbox);
```
Force unchecking `checkbox`

---

```c
int			display_checkbox(t_bunny_pixelarray	*pix,
					 t_checkbox		*checkbox,
					 t_bunny_pixelarray	*font,
					 t_bunny_pixelarray	**png_checkbox);
```
update the graphics of `checkbox` inside `pix`, with `font` and `png_checkbox` graphics

---

```c
void			tekgui_show(t_tekgui		*gui);
```
Open a window a show the `gui`

---

```c
t_bunny_pixelarray	*stretch(t_bunny_pixelarray	*oldpixel,
				 int			newx,
				 int			newy);
```
Stretch an an image inside `oldpixel` to be resize to `newx, newy`

---

```c
t_progressbar		*progressbar_get(t_tekgui *gui, char *name);
```
Get a progressbar by its `name`

---

```c
int			progressbar_setprogress(t_tekgui		*gui,
						t_progressbar		*progressbar,
						int			progress);
```
Set the `progressbar` progress to `progress`

---

```c
int			progressbar_getprogress(t_progressbar *progressbar);
```
get the current progress from a `progressbar`

---

```c
int			display_prgrsbar(t_bunny_pixelarray	*pix,
					 t_progressbar		*prgrsbar);
```
Force update graphic of `prgrsbar inside `pix`

---

```c
t_button		*button_get(t_tekgui *gui, char *name);
```
Get a `t_button` from its `name`

---

```c
int			button_settext(t_tekgui		*gui,
				       t_button		*button,
				       char		*text);
```
Set the `text` of a `button`

---

```c
char			*button_gettext(t_button *button);
```
Get the text of a `button`

---

```c
char			*checkbox_gettext(t_checkbox *checkbox);
```
Get the text of a `t_checkbox`

---

```c
t_checkbox		*checkbox_get(t_tekgui *gui, char *name);
```
Get a `t_checkbox` from its name

---

```c
int			checkbox_settext(t_tekgui	*gui,
					 t_checkbox	*checkbox,
					 char		*text);
```
Set the `text`  of a `checkbox`

---

```c
t_image			*image_get(t_tekgui *gui, char *name);
```
Retrieve a `t_image` from a `name`

---

```c
char			*image_getsrc(t_image *image);
```
Get the image `src`

---

```c
int			image_setsrc(t_tekgui	*gui,
				     t_image	*image,
				     char	*src);
```
Set the `image` `src`

---

```c
int			display_label(t_bunny_pixelarray	*pix,
				      t_label			*label,
				      t_bunny_pixelarray	*font);
```
Force update graphics of a `t_label`

---

```c
t_textbox		*textbox_get(t_tekgui *gui, char *name);
```
retrieve `t_textbox` from its `name`

---

```c
char			*textbox_gettext(t_textbox *textbox);
```
Get text of a `t_textbox`

---

```c
int			textbox_settext(t_tekgui	*gui,
					t_textbox	*textbox,
					char		*text);
```
Set the text of a `t_textbox`

---

```c
int			display_image(t_bunny_pixelarray	*pix,
				      t_image			*image,
				      int			mode);
```
Force update the graphic of a `t_image`

---

```c
char			*getfield_safe(t_bunny_ini *ini,
				       char *scope,
				       char *field,
				       int index);
```
Get a field from a `ini` with error management

Macros
===

### Checkbox

You can check if the state of a checkbox is equal to `CHECKED` `UNCHECKED`

### Image

There are different size mode for images :

`STRETCHMODE_FILL` : The image fille the `size` in any way
`STRETCHMODE_NONE` : The image is loaded normaly. If the `size` is bigger than the image, it is sticked at the top-left. If the `size` is smaller, the image is cropped
`STRETCHMODE_CENTER` : The image is loaded normaly. If the `size` is bigger than the image, it is sticked at the center. If the `size` is smaller, the image is cropped

Structures
===

### `t_size`

```c
int		width;
int		height;
```
`width` : **integer** : the width of the size
`height` : **integer** : the height of the size

### `t_text`

```c
char                *text;
int                 size;
t_bunny_position    position;
t_color             color;
t_bunny_pixelarray  *pix;
```
**char \*** `text` : the text that will be printed
**t_size** `size` : the size of the component
**t_bunny_position** `position` : the position of the component
**t_color** `color` : the color of the text
**t_bunny_pixel_array \*** `pix` : the pixelarray where the text will be dislpayed

### `t_button`

```c
char			*name;
t_bunny_position	pos;
t_size		size;
t_color		borderColor;
int			borderSize;
t_color		innerColor;
char			*text;
int			fontSize;
t_color		fontColor;
ptrfct 		onclick;
ptrfct 		onhover;
```

**char \*** `name` : the name of the button

**t_bunny_position** `pos` : The position of the button

**t_size** `size` : The size of the button

**t_color** `borderColor` : The color of the border of the button

**integer** `borderSize` : The size of the button's border (in pixels)

**t_color** `innerColor` : The button's inner color

**char \*** `text` : The text of the button

**integer** `fontSize` : the font size of the button's text

**t_color** `fontColor` : The color of the button's text

**ptrfct** `onclick` : The function called when the `onclick` event occurs

**ptrfct** `onhover` : The function called when the `onhover` event occurs

### `t_label`

```c
char			*name;
char			*text;
t_color		color;
int			size;
t_bunny_position	pos;
```

**char \***     `name` : The name of the label
**char \***     `text` : The text of the label
**t_color**		`color` : The text color of the label
**int**			`size` : The size of the label
**t_bunny_position**	`pos` : The position of he label

### `t_checkbox`

```c
char			*name;
int			state;
t_size		size;
t_color		backcolor;
ptrfct 		oncheckstatechanged;
t_label		*label;
```

**char \***			`name` : The name of th checkbox
**int**			`state` : The current state of the checkbox
**t_size**		`size` : The size of the checkbox
**ptrfct** 		`oncheckstatechanged` : The function called when the `oncheckstatechanged` event occurs
**t_label \***		`label` : The label linked to the checkbox

### `t_progressbar`

```c
char			*name;
t_bunny_position	pos;
t_size		size;
t_color		borderColor;
int			borderSize;
t_color		backColor;
t_color		barColor;
int			value;
int			max;
int			min;
t_label		attached_text;
```

**char \***			`name`

* The name of the progressbar

**t_bunny_position**	`pos`

* The position of the progressbar

**t_size**		`size`

* The size of the progressbar

**t_color**		`borderColor`

* The color of the progressbar border

**int**			`borderSize`

* The size of the progressbar's border

**t_color**		`backColor`

* The back color of the progressbar

**t_color**		`barColor`

* The color of the progressbar's bar

**int**			`value`

* The current value of the progressbar

**int**			`max`

* The max value of the progressbar

**int**			`min`

* The minimum value of the progressbar

**t_label**		`attached_text`

* The text attached to the progressbar



### `t_textbox`
```c
char			*name;
t_bunny_position	pos;
t_size		size;
t_color		borderColor;
int			borderSize;
t_color		innerColor;
char			*text;
char			*placeholder;
t_color		placeholder_color;
int			fontSize;
t_color		fontColor;
ptrfct 		onclick;
ptrfct 		onhover;
ptrfct		ontextchanged;
int			waiting_for_text;
```

**char \***			`name` : The name
**t_bunny_position**	`pos` : The position
**t_size**		`size` : The size
**t_color**		`borderColor` : The border color
**int**			`borderSize` : The border size
**t_color**		`innerColor` : The inner coloor
**char \***			`text` : The predefined text
**char \***			`placeholder` : the placeholder (Appear if no text is typed)
**t_color**		`placeholder_color` : The placeholder font color
**int**			`fontSize` : The text font size
**t_color**		`fontColor` : The text font color
**ptrfct** 		`onclick` : The function called when the `onclick` event occurs
**ptrfct** 		`onhover` : The function called when the `onhover` event occurs
**ptrfct**		`ontextchanged` : The function called when the `ontextchanged` event occurs
**int**			`waiting_for_text` : Set to 1 if the textbox is waiting text *i.e.* the textbox is selected


### `t_image`

See the [Image macros](/en/function_list/#image)

```c
char			*name;
int			borderSize;
t_color		borderColor;
char			*src;
t_size		size;
t_bunny_position	pos;
ptrfct		onclick;
```

**char \***			`name` : The name
**int**			`borderSize` : the size of the border
**t_color**		`borderColor` : The color of the border
**char \***			`src` : The path to the image source
**t_size**		`size` : The size of the frame where the image will be displayed
**t_bunny_position**	`pos` : The position
**ptrfct**		`onclick` : The function called when the `onclick` event occurs

### `t_tekgui`
```c
struct s_tekgui	*child_win;
int			child_win_nbr;
t_button		*buttons;
int			buttons_nbr;
t_checkbox		*checkboxs;
int			checkboxs_nbr;
t_progressbar		*progressbars;
int			progressbars_nbr;
t_label		*labels;
int			labels_nbr;
t_textbox		*textboxs;
int			textboxs_nbr;
t_image		*images;
int			images_nbr;
t_bunny_ini		*config;
t_size		size;
t_bunny_window	*win;
char			*name;
t_bunny_pixelarray	*pix;
t_color		bgcolor;
t_bunny_pixelarray	*font;
t_bunny_pixelarray	**png_checkbox;
t_callback_list	callback;
double		progress;
void			*userdata;
```

**struct s_tekgui	\***`child_win` : A pointer to windows child of the main window
**int** `child_win_nbr` : The number of child windows
**t_button \***`buttons` : A pointer to the buttons
**int** `buttons_nbr` : The number of buttons
**t_checkbox \*** `checkboxs` : A pointer to the checkboxs
**int** `checkboxs_nbr` : The number of checkboxs
**t_progressbar \*** `progressbars` : A pointer to the progressbars
**int** `progressbars_nbr` : The number of progressbars
**t_label \*** `labels` : A pointer to the labels
**int** `labels_nbr` : The number of labels
**t_textbox \*** `textboxs` : A pointer to the textboxs
**int** `textboxs_nbr` : The number of textboxs
**t_image \*** `images` : A pointer to the images
**int** `images_nbr` : The number of images
**t_bunny_ini \*** `config` : The current config file
**t_size** `size` : The window original size
**t_bunny_window \*** `win` : The `t_buny_window` component (for sharing)
**char \*** `name` : The window name
**t_bunny_pixelarray \*** `pix` : The render `pixelarray`
**t_color** `bgcolor` : The background color
**t_bunny_pixelarray \*** `font` : The font file
**t_bunny_pixelarray \*\*** `png_checkbox` : The checkbox image ressource
**void \*** `userdata` : The variable where the user can put his datas


Tips and tricks
===

You can define colors in several ways
If you have an `unsigned int` : 0xff0000
But you need a `t_color`, you can simply do this :
```c
t_color color;
unsigned int c;

c = 0xff0000;
color.full = c;
```
It will convert your `unsigned int` to a `t_color`
In reverse you can do this too

```c
t_color color;
unsigned int c;

color.argb[0] = 255;
color.argb[1] = 0;
color.argb[2] = 0;
c = color.full;
```
