

# [Halfmoon](https://www.gethalfmoon.com)

This is a re-write / custom design of the now abandoned half moon css project.

# New Features

# Form Input Icons

Now supports using icons on form field inputs.

Add class 'with-icon-{parameter}' to form field class :

The icon is wrapped in a <span> element. By defualt we are using font awesome but any icon libaries will work. You may need to adjust the offset in the css file when accomodating for differnt size icons form field padding etc..

It can take the Before or After Parameter to place the icon at the start or end of the input field.

```html
<input type="password" class="form-control mb-5 with-icon-after" id="password" name="password">

<span class="fa-solid fa-eye-slash input-icon-after"></span>
```


