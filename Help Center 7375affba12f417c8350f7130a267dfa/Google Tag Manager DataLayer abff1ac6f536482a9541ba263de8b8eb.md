# Google Tag Manager DataLayer

This is an advanced tutorial and proceed only if understand the risks.

## Getting your Theme Ready

1. Create a new file `sellify-ucd-gtm.liquid` in `snippets` of your [Shopify Theme](https://shopify.com/admin/themes/current). Copy and Paste the following code and `Save`

```jsx
<script>
  (function(){
    function addToCart(event, lineItem, quantity, price){
        sellify.ucd.dataLayer = sellify.ucd.dataLayer || window.dataLayer || [];

        sellify.ucd.dataLayer.push( {
            'event': 'addToCart',
            'ecommerce': {
                'currencyCode': sellify.ucd.cart.currency,
                'add': {
                    'products': [
                        {
                            'name': lineItem.product_title,
                            'id': lineItem.product_id,
                            'price': typeof price !== "undefined" ? price / 100 : lineItem.line_price / 100,
                            'brand': lineItem.vendor,
                            'category': lineItem.product_type,
                            'variant': lineItem.variant_title || '',
                            'quantity': quantity,
                        }
                    ]
                }
            }
        } );
    }

    function removeFromCart(event, lineItem, quantity, price){
        sellify.ucd.dataLayer = sellify.ucd.dataLayer || window.dataLayer || [];

        sellify.ucd.dataLayer.push( {
            'event': 'removeFromCart',
            'ecommerce': {
                'currencyCode' : sellify.ucd.cart.currency,
                'remove': {
                    'products': [
                        {
                            'name': lineItem.product_title,
                            'id': lineItem.product_id,
                            'price': typeof price !== "undefined" ? price / 100 : lineItem.line_price / 100,
                            'brand': lineItem.vendor,
                            'category': lineItem.product_type,
                            'variant': lineItem.variant_title || '',
                            'quantity': quantity,
                        }
                    ]
                }
            }
        } );
    }

    window.addEventListener( "Sellify::UCD::ItemAdded", function( e ){
	      addToCart(e.detail, e.detail.line_item, e.detail.line_item.quantity);
    } );

    window.addEventListener( "Sellify::UCD::ItemChanged", function( e ){
        sellify.ucd.dataLayer = sellify.ucd.dataLayer || window.dataLayer || [];
        const previousLineItem = e.detail.previous_cart.items[e.detail.line - 1];

        var lineItem = null;
        if( e.detail.quantity > 0 )
        {
            lineItem = e.detail.cart.items[e.detail.line - 1];

            if( lineItem.quantity > previousLineItem.quantity )
            {
                addToCart( e.detail, lineItem, lineItem.quantity - previousLineItem.quantity, lineItem.line_price - previousLineItem.line_price  );
            }
            else if( lineItem.quantity < previousLineItem.quantity )
            {
                removeFromCart( e.detail, lineItem, previousLineItem.quantity - lineItem.quantity, previousLineItem.line_price - lineItem.line_price );
            }

        }
        else if( e.detail.previous_cart )
        {
            lineItem = e.detail.previous_cart.items[e.detail.line - 1];
            removeFromCart( e.detail, lineItem, previousLineItem.quantity, previousLineItem.line_price );
        }
    } );
})();
</script>
```

2. Include `sellify-ucd-gtm.liquid` in your [theme.liquid](https://shopify.com/admin/themes/current?key=layout%2Ftheme.liquid) using the following code:

```html
{% include 'sellify-ucd-gtm' %}
```

## Getting Google Tag Manager Ready

You have to create a few tags and triggers in your Google Tag Manager account. Please create tags and trigger similar to the following screenshots:

1. addToCart Tag:

    ![Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled.png](Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled.png)

2. addToCart Trigger

    ![Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%201.png](Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%201.png)

3. removeFromCart Tag

    ![Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%202.png](Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%202.png)

4. removeFromCart Trigger

    ![Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%203.png](Google%20Tag%20Manager%20DataLayer%20abff1ac6f536482a9541ba263de8b8eb/Untitled%203.png)