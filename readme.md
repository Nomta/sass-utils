# Sass Utils
*Basic classes and mixins for Sass.*  

It contains three modules:
- [base](#base) - reset styles and several useful classes, such as clearfix.
- [mixins](#mixins) - frequently used mixins.
- [utils](#utils) - commonly used css classess.

All the modules are included in `main.scss` or you can include them separately.

The settings are in the `variables`.

### Base
It resets the styles of the most-used tags and adds the most common classes. Some lines are commented out. Uncomment them to apply a reset or the required classes.

Classes:
- video: determines the routine aspect ratio of 16:9
- clearfix: clears the float
- ellipsis: adds an ellipsis to the single-line text when truncating 
- hidden: `display: none` for the element
- visible: `display: block` for the element
- invisible: makes the element invisible via `opacity: 0` when it is not hovered

### Mixins
Сontains the most commonly used snippets of css rules. Allows you to shorten the writing of rules by specifying the default property values.

#### Usage 
```
/* Before */ 

    bg-image: url(image.png);    // and other background values
  

/* After */

    background: url(image.png) no-repeat;   // and other background values
    background-size: cover;


/* Before */ 

    bg-mask(rgba(255, 0.1));  // makes a mask over an element
                             // optional parameters: transition-duration, content
                         
/* After */

    position: relative;
    &:after {
      content: '';
      display: block;
      height: 100%;
      width: 100%;
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 2;
      background: rgba(255, 255, 255, 0.1);
    }

/* Before */ 

    flex-row();        // optional parameters: justify-content, align-items
  

/* After */

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: stretch;
  

/* Before */ 

    flex-column();        // optional parameters: justify-content, align-items
  

/* After */

    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: stretch;

```

### Utils
It adds the most common classes. Some lines are commented out. Uncomment them to apply the ones you need.

Classes:
- display: d-block, d-inline-block, d-table
- position: pos-static, pos-rel, pos-abs
- hidden (display: none)
- sizes: w-100 (width: 100%), h-100 (height: 100%)
- border-radius: rounded (50%), rounded-pill (5px)

Commented out:
- video: determines the routine aspect ratio of 16:9
- clearfix: clears the float
- ellipsis: adds an ellipsis to the single-line text when truncating 
- hidden: `display: none` for the element
- visible: `display: block` for the element
- invisible: makes the element invisible via `opacity: 0` when it is not hovered

[learn more](./utils)

*[back to top](#sass-utils)*  

### License
This project is available under the [MIT](./license) license.  