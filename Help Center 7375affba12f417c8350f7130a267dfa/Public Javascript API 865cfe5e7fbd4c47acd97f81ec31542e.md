# Public Javascript API

- **Open cart drawer**

    ```jsx
    sellify.ucd.helpers.ajaxCart.show();
    ```

- **Open cart drawer with fresh cart data**

    ```jsx
    sellify.ucd.helpers.ajaxCart.load();
    ```

    Any element having class `open-drawer` or `href="/cart"` will open the drawer when clicked.

- **Build cart drawer when you already have cart object**

    ```jsx
    // Build cart and open the drawer
    sellify.ucd.helpers.ajaxCart.buildCart(cart);

    // Build cart but do not open the drawer
    sellify.ucd.helpers.ajaxCart.buildCart(cart, false);
    ```

- **Close cart drawer**

    ```jsx
    sellify.ucd.helpers.ajaxCart.hide();
    ```

    You can add a class `close-drawer` to a button/link. Clicking on that button/link will hide the drawer.

- **Check if cart drawer is visible**

    ```jsx
    // Returns true if visible
    sellify.ucd.helpers.ajaxCart.visible();
    ```

- **Check if cart drawer is hidden**

    ```jsx
    // Returns true if visible. Notice the ! at start
    ! sellify.ucd.helpers.ajaxCart.visible(); 
    ```

- **Get jQuery instance**

    ```jsx
    const jQuery = sellify.ucd.jquery();
    ```

- **Get raw/original cart data**

    ```jsx
    const cart = sellify.ucd.original_cart;
    ```