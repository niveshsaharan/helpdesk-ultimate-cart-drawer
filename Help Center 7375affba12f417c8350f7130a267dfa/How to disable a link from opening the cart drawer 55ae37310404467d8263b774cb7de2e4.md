# How to disable a link from opening the cart drawer?

Cart drawer doesn't open the cart drawer for an HTML element if it has an attribute `data-ucd="0"` 

```html
<!-- Does not open cart drawer -->
<a href="/cart" data-ucd="0">Cart</a>

<!-- Opens cart drawer -->
<a href="/cart">Cart</a>
```

Any element having class `open-drawer` will open cart drawer.