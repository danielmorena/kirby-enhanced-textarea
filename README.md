# Kirby Enhanced Textarea v1.4

This textarea extends the built-in textarea without reinventing the wheel. Handy and customizable headline functions, intelligent list buttons and a custom page selector make editing textareas a breeze.

![Preview](https://cloud.githubusercontent.com/assets/7975568/26103764/44eb2fc4-3a3b-11e7-87dc-86b328f22f85.gif)

## Installation

Download or clone this repository, put the folder into your `site/fields` folder and rename it to `textarea`. Alternatively you can also use the [Kirby CLI](https://github.com/getkirby/cli).

## Configuration

### Headlines

You can change the headline buttons to any headline from 1-6 in the `site/config.php`. The function, the shortcut (meta+1, meta+2, ...) as well as the icon number will adjust accordingly.

Example:
````
c::set('textarea.h1', 'h2');
c::set('textarea.h2', 'h3');
c::set('textarea.h3', 'h4');
````

### Buttons

You can globally define default buttons for any textarea on your site by setting the `textarea.buttons` variable in your `config.php`. By default the buttons `h2` (headline 2), `h3` (headline 3), `bold`, `italic`, `ulist` (unordered list), `olist` (ordered list), `link`, `page` and `email` are displayed. There's also a `blockquote` and `h1` button you can use.

````
c::set('textarea.buttons', array(
  "h1"
  "blockquote",
  "link",
  "page"
));
````


If you want to override this for a single field just use `buttons:` as you would with the built-in textarea:

````
test:
  type: textarea
  buttons:
    - h1
    - h2
    - bold
    - olist
    - link
````
