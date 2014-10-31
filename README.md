
![](http://atomgroomdesign.github.io/liquid-grid/img/Liquid-Grid-Logo.png)

# Liquid Grid - A grid with no constraints.

The Liquid Grid system was to designed fill the viewport and to flex evenly with it. Rather than definining random breakpoints, or set widths, Liquid Grid aims get rid of the entire idea of fixed layouts.

Liquid Grid is a _side project_ of [Atom Groom](http://www.atomgroom.com). I will to the best of my ability work to fix bugs and support requests.  As an open-source project you are highly encouraged to contribute to the project.  I wrote a [blog article](http://www.atomgroom.com/thoughts/the-return-of-full-width-design) about this vision.  Please read it to ensure your contributions and requests are inline with the goals of this project.

The Liquid Grid highlights:

*   Uses LESS
*   Percentage based layout.
*   Semantic mixins - you decide the column ratios
*   Nestable
*   You control breakpoints
*   Check out a [live demo here](http://atomgroomdesign.github.io/liquid-grid/demo/).


* * *

### Project Setup 

* Clone or download Liquid Grid LESS files locally
* Setup LESS Build (your choice on how you do this - Grunt, Gulp, CDN JS, etc.)
* Include the compiled LESS or CSS in your project's < head > 
* Start coding!

* * *

### Example LESS Mixin Use:

In the first value we define amount of columns in a row.  In the second value we define the total amount of colums in the row.  In this case, 1 / 2 = 50%

```
.class-name {
	.grid-column(1,2);
}
```

### Example Markup:

```
	<div class="row">
		<section class="class-name"></section>
	</div>
```

* * *

### Other Goodies

#### Breakpoints
<h4>Breakpoints</h4>
Use a media query as mixin with the variables that I have setup to create your own unique set of breakpoints, per element. You can adjust the variables that I setup in the variables.less file.

```
.class-name {
	.grid-column(1,2);
    @media(max-width:@breakpoint-xs){
      .grid-column(1,1);
    }
}
```

#### Grid Helpers

I have worked with a lot of different grid systems and one thing that I did not like is padding implementations. I discovered that I could easily make a mixin with variables and then add that semantically to each class as needed.

I found that any particular site or app that I was working on had similar uses of padding throughout project.  Therefore, rather than repeating myself I could implement a set of variables with a mixin. This then speeds my work flow and the overall consistency of spacing.

#### Example LESS:

```
.class-name {
	.grid-column(1,2);
	.b-padding--horz(@grid-max-value,@grid-max-value); // left,right
	.b-padding--vert(@grid-min-value,@grid-min-value); // top, bottom
}
```

#### Vertical Centering

Add the mixin as displayed below. I use the display: table and table cell technique to achieve vertical centering. 

```
.class-name {
	.vertical-align;
}
```

#### Horizontal Centering

Add the mixin as displayed below. 

```
.class-name {
	.col--centered;
}
```

* * *

### Media

#### Images

By placing an image within any of your markup that uses a grid mixin the image will automatically fill and flex with the width of the column.

```
	<section class="class-name">
		<img src="http://placehold.it/350x150" />
	</section>
```

#### Video

To insert a flexible video into a column, place a containing DIV around the embeded iframe with the class "video-container".

```
	<section class="class-name">
      <div class="video-container">
          <iframe src="" frameborder="0" allowfullscreen></iframe>
      </div>
    </section>
```

#### Google Maps

To insert a flexible Google Map into a column, place a containing DIV around the embeded iframe with the class "google-maps".

```
	<section class="class-name">
      <div class="google-maps">
          <iframe src="" frameborder="0" allowfullscreen></iframe>
      </div>
    </section>
```    

* * *

### Awesome GIF Demo

![screen cast demo of liquid grid](http://atomgroomdesign.github.io/liquid-grid/img/liquid-grid-screencast.gif)

This project is maintained by [atomgroomdesign](https://github.com/atomgroomdesign)

* * *

### Live Demo
Check out a [live demo here](http://atomgroomdesign.github.io/liquid-grid/demo/).

* * *


#### Author

Atom Groom

* * *

#### Copyright and license

Copyright 2013 Atom Groom.

Licensed under the MIT License:
http://opensource.org/licenses/MIT
    