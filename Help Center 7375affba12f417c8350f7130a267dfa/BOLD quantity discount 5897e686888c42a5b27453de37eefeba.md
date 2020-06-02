# BOLD quantity discount

1. Add following code in ULTIMATE Cart Drawer's `Custom Javascript` field on [Settings page](https://ucd.sellifyapps.com/settings) and Save:

    ```jsx
    /* BOLD's quantity discount */
    sellify.ucd.filters.cart.push( function( cart ){
    	if( typeof BOLD === "object" && typeof BOLD.common === "object" && typeof BOLD.common.cartDoctor === "object" && typeof BOLD.common.cartDoctor.fix === "function" )
    	{
    		 return BOLD.common.cartDoctor.fix( cart )
    	}
    	
    	return cart;
    });
    /* /BOLD's quantity discount */
    ```

2. Test through.