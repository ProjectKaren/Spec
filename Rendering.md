# Rendering Section

`dom-tree` -> `render-tree`

### DOM Element

Slots  
* `ident` keyword
* `name` string
* `attributes` (keyword . css-value) a-list
* `parent` dom-element | nil
* `children` dom-element list
* `previous` dom-element | nil
* `next` dom-element | nil

The `ident` can be taken `html`, `body`, `h1`, `a`, and so on.

#### CSS Value

Slots  
* `data` any
* `unit` keyword | nil

The `unit` can be taken `px`, `%`, `em`, `vw`, `vh`, and so on.


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
* `background` renderer-box-fill | nil
* `margin` renderer-box-fill | nil
* `padding` renderer-box-fill | nil
* `border` renderer-box-stroke | nil
* `text` renderer-text | nil


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
* `anchor` (float . render-style) a-list
