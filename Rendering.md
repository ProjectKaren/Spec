# Rendering Section

`dom-tree` -> `render-tree`

### DOM Element

Slots  
* `name` keyword
* `attributes` (keyword . css-unit) a-list
* `parent` dom-element
* `children` dom-element list
* `previous` dom-element
* `next` dom-element

#### CSS Value

Slots  
* `value` any
* `sign` keyword

The `sign` can be taken `px`, `%`, `em`, `vw`, `vh`, and so on.


### Render Object

Slots  
* `dom` dom-element
* `style` render-style
* `clip` clip-layer
* `animation` (css-animation . keyword) a-list

Associate  
* `recalc`  
  Recalculate style of render object. This function destructively changes the `style` and the `clip` depending on the `animation` and the attributes of `dom`.  
* `render`  
  Render and clip the render object.  


#### Render Style

Slots  
* `background` renderer-box-fill nil
* `margin` renderer-box-fill nil
* `padding` renderer-box-fill nil
* `border` renderer-box-stroke nil
* `text` renderer-font nil


#### Clip Layer

Slots  
* `x-mode` keyword
* `y-mode` keyword
* `x` float
* `y` float
* `width` float
* `height` float


#### CSS Animation

Slots  
* `name` string
* `phase` (float . render-style) a-list
