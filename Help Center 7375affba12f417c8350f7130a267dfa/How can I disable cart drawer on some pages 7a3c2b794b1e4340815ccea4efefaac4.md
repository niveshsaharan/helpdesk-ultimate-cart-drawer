# How can I disable cart drawer on some pages?

You can add following meta tag to the pages you want to hide the drawer from.

```html
<meta name="sellify:ucd:active" content="false" />
```

### How to add the meta tag in your published theme?

---

1. Open [`theme.liquid`](https://shopify.com/admin/themes/current?key=layout%2Ftheme.liquid) in your Shopify admin.
2. Add the meta tag code provided above before ending `</head>`

If you add the above code without any condition, Cart drawer won't work on any of the page. It can be useful when you want to disable it from one/some of your themes.

### How to add the meta tag in one of your unpublished theme?

---

1. Visit [`Themes`](https://shopify.com/admin/themes) page in your Shopify admin.
2. Click on 'Actions' in front of your unpublished and click '**Edit Code**' in the dropdown.
3. Click `theme.liquid` from `Layout` directory.
4. Add the meta tag code provided above before ending `</head>`

## Code Examples

---

### Disable cart drawer on products page

```html
{% if template.name == 'product' %} 
	<meta name="sellify:ucd:active" content="false" /> 
{% endif %}
```

### Disable cart drawer on collections page

```html
{% if template.name == 'collection' %} 
	<meta name="sellify:ucd:active" content="false" /> 
{% endif %}
```

### Disable cart drawer on cart page

```html
{% if template.name == 'cart' %} 
	<meta name="sellify:ucd:active" content="false" /> 
{% endif %}
```