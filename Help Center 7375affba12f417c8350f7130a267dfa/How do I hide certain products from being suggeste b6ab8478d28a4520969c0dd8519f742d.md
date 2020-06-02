# How do I hide certain products from being suggested in Upsells/Automatic Recommendations?

ULTIMATE Cart Drawer doesn't suggest `Out of Stock` items by default.

- By adding a tag to the product

    If you need to hide certain products i.e. Gift cards or any other product, all you have to do is add a tag `ucd-hidden` to those products in your store and Cart drawer will no longer show `ucd-hidden` tagged items in any of the suggestions.

- Conditionally/Programmatically hide a product

    If you have some programmatic/conditional requirements on which you want to hide a product, you can add following code in `Custom Javascript` field on the `settings` page.

    ```jsx
    sellify.ucd.filters.hide_product.push(function(product) {
    	
    	// return false: Do not hide the product
    	// return true: Hide the product
    	return false;
    });
    ```

    Example:

    ```jsx
    sellify.ucd.filters.hide_product.push(function(product) {

    	// Hide Free Gift product from suggestions
    	if(product.title === 'Free Gift')
    	{
    		return true;
    	}

    	// Hide product if it has tag some-tag
    	if(product.tags.includes('some-tag'))
    	{
    		return true;
    	}

    	// Do not hide this product
    	return false;
    });
    ```