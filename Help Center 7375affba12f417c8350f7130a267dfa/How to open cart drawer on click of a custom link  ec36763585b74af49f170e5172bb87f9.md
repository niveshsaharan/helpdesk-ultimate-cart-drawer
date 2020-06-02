# How to open cart drawer on click of a custom link or button?

- Add a class `open-drawer` to any HTML element (Link, button, div, span etc.).

    ```html
    <button class="open-drawer">Open Drawer</button>
    ```

- Any link having `href="/cart"` will open the cart drawer

    ```html
    <a href="/cart">Cart</a>
    ```

- Open cart drawer programmatically

    ```jsx
    // It opens the cart drawer with existing cart data
    sellify.ucd.helpers.ajaxCart.show(); 

    // If you need to open cart drawer fresh cart data
    sellify.ucd.helpers.ajaxCart.load();
    ```