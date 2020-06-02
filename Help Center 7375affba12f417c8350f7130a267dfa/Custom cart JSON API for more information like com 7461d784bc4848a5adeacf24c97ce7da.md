# Custom cart JSON API for more information like compare_at_price for items in cart

This is an advanced tutorial and proceed only if understand the risks.

Shopify's Ajax API for cart is missing some fields like compare_at_price and inventory details for items in cart. And for some merchants, it is important to show those details in cart drawer.

1. Create a new file `index.ucd.liquid` in `templates` of your [Shopify Theme](https://shopify.com/admin/themes/current). Copy and pate the following code and Save:

    ```json
    {%- layout none -%}
    { 
      "cart":  {{ cart | json }},
      "items": [
          {%- for item in cart.items -%}
          {
            "variant": {{ item.variant | json }},
            "product": {{ item.product | json }},
            "inventory_quantity": {{ item.variant.inventory_quantity | times: 1 }},
            "inventory_policy": {{ item.variant.inventory_policy | json }},
            "compare_at_price": {{ item.variant.compare_at_price | times: 1  }},
            "compare_at_price_formatted": {{ item.variant.compare_at_price | money | json }}
          }{%- if forloop.last != true -%},{%- endif -%}
          {%- endfor -%}
        ]
    }
    ```

2. Add following code in ULTIMATE Cart Drawer's `Custom Javascript` field on [Settings page](https://ucd.sellifyapps.com/settings) and Save:

    ```jsx
    /* Custom Cart JSON API */
    sellify.ucd.cart_path = '/?view=ucd';

    sellify.ucd.filters.raw_cart.push(function(cart){
      if (sellify.ucd.cart_path.includes('view=ucd')) {
        cart.cart.items = cart.cart.items.map(function(item, index){
          item = {...cart.items[index], ...item };

          return item;
        });
        return cart.cart;
      }
      
      return cart;
    });
    /* /Custom Cart JSON API */
    ```

3. Test through.