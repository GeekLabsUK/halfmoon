

# [Halfmoon](https://www.gethalfmoon.com)

This is a re-write / custom design of the now abandoned half moon CSS project.

## New Features

### Form Input Icons

Halfmoon now supports using icons on form field inputs. To add an icon to a form field, add the class `with-icon-{parameter}` to the form field class.

The icon is wrapped in a `<span>` element. By default, Halfmoon uses Font Awesome, but you can use any icon library. You may need to adjust the offset in the CSS file to accommodate different size icons, form field padding, etc.

The `{parameter}` can be `before` or `after` to place the icon at the start or end of the input field.

```html
<!-- Icon at the end of the input field -->
<input type="password" class="form-control mb-5 with-icon-after" id="password" name="password">
<span class="fa-solid fa-eye-slash input-icon-after"></span>

<!-- Icon at the start of the input field -->
<input type="password" class="form-control mb-5 with-icon-before" id="password" name="password">
<span class="fa-solid fa-eye-slash input-icon-before"></span>
```

### Toggle Password Visibility

By using the `with-icon` class, you can now use an icon to toggle the visibility of a password field by using the `halfmoon.togglePassword('password', this)` onclick handler.

```html
<!-- Toggle the password field with ID "password" -->
<span id="togglePassword" class="fa-solid fa-eye-slash input-icon-after" onclick="halfmoon.togglePassword('password', this)"></span>
```
To toggle multiple password fields, pass the ID of each password field to the onclick handler:

```html
<!-- Toggle password field with ID "password" -->
<input type="password" class="form-control mb-5 with-icon-before with-icon-after" id="password" name="password" placeholder="Please enter your password">
<span id="togglePassword" class="fa-solid fa-eye-slash input-icon-after" onclick="halfmoon.togglePassword('password', this)"></span>

<!-- Toggle password field with ID "passwordconfirm" -->
<input type="password" class="form-control mb-5 with-icon-before with-icon-after" id="passwordconfirm" name="passwordconfirm" placeholder="Please confirm your password">
<span id="togglePassword" class="fa-solid fa-eye-slash input-icon-after" onclick="halfmoon.togglePassword('passwordconfirm', this)"></span>
```

### Fake Content Styles

Sometimes, especially when building out admin templates, it's useful to have some way of depicting fake content. The same as used in the Halfmoon docs seen [here](https://www.gethalfmoon.com/page-sections-demo/?sidebar-type=overlayed-sm-and-down&show-alert=yes).

The following CSS classes have been added:

```css
.fake-window .fake-window-top-row {
  padding: 1rem;
  background-color: #ecf0f1;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  border-top-left-radius: 0.4rem;
  border-top-right-radius: 0.4rem;
}

.dark-mode .fake-window .fake-window-top-row {
  background-color: rgba(0, 0, 0, 0.1);
}

.fake-button {
  display: inline-block;
  width: 1.6rem;
  height: 1.6rem;
  border-radius: 50%;
  margin-top: 0.5rem;
  margin-right: 0.5rem;
}

.fake-button:after {
 
.fake-button:after {
  content: '\200b';
}

.fake-content {
  height: 1.4rem;
  background-color: #ecf0f1;
  border: 1px solid rgba(0, 0, 0, 0.15);
  margin-bottom: 1rem;
  border-radius: 0.2rem;
}

.dark-mode .fake-content {
  background-color: rgba(255, 255, 255, 0.1);
  border-color: rgba(255, 255, 255, 0.025);
}

.fake-content:after {
  content: '\200b';
}

.fake-content:last-child {
  margin-bottom: 0;
}
```







             




