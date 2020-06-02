# Cart link sometimes redirect to cart page instead of opening the drawer

App scripts registered by Shopify apps' are loaded once the page is loaded successfully and it causes delay in loading of cart drawer. You can add the following line of code in your [theme.liquid](https://shopify.com/admin/themes/current?key=layout/theme.liquid) file before ending `</head>` tag and it will start opening the cart drawer all the times:

```html
<!-- ULTIMATE Cart Drawer -->
<script type="text/javascript" 
				async="async"
				src="https://cdn.shopify.com/s/files/1/2325/8929/t/1/assets/ultimate-cart-drawer___app.js?shop={{shop.permanent_domain}}&t={{ 'now' | date: "%Y%m%d"}}-01"></script>
<!-- /ULTIMATE Cart Drawer -->
```