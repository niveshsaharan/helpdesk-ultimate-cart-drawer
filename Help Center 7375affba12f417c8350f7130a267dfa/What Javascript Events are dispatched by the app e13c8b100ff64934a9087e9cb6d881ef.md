# What Javascript Events are dispatched by the app?

ULTIMATE Cart Drawer is designed to be a developer friendly app. It dispatches events for various actions it takes so you can do your own thing at certain points. Here are all the events:

- **Initialized**

    This event is dispatched when the cart drawer is initialised. It is dispatched once per page load.

    ```jsx
    window.addEventListener('Sellify::UCD::Initialized', function(e){
      console.log('Cart drawer is initialized and ready to use.')
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
        }
        ```

- **BeforeCartBuilt**

    ```jsx
    window.addEventListener("Sellify::UCD::BeforeCartBuilt", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "cart": {
            "token": "b9983eaec617fee4c98cc8213804ac9d",
            "note": null,
            "attributes": {},
            "original_total_price": 82700,
            "total_price": 82700,
            "total_discount": 0,
            "total_weight": 907.0033,
            "item_count": 1,
            "items": [
              {
                "id": 12543478169683,
                "properties": {
                  "__ucd": "Upsells"
                },
                "quantity": 1,
                "variant_id": 12543478169683,
                "key": "12543478169683:ee62fe287b247705ef707d2a44168db0",
                "title": "DZR Minna - 42",
                "price": 82700,
                "original_price": 82700,
                "discounted_price": 82700,
                "line_price": 82700,
                "original_line_price": 82700,
                "total_discount": 0,
                "discounts": [],
                "sku": "Shoes - DZR - Minna - 42",
                "grams": 907,
                "vendor": "DZR",
                "taxable": true,
                "product_id": 1351134412883,
                "product_has_only_default_variant": false,
                "gift_card": false,
                "final_price": 82700,
                "final_line_price": 82700,
                "url": "/products/dzr-minna?variant=12543478169683",
                "featured_image": {
                  "aspect_ratio": 1.5,
                  "alt": "DZR Minna",
                  "height": 1365,
                  "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                  "width": 2048
                },
                "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                "handle": "dzr-minna",
                "requires_shipping": true,
                "product_type": "Shoes",
                "product_title": "DZR Minna",
                "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesDZR’s all-time best seller, the Minna is proudly named after the gritty S.F. alley their showroom calls home. Understated tones, locally designed graphics, and a Variable Flex Shank combine to create a sneaker that’s as classic in its style as it is comfortable mashing on pedals.\n\nSpecs\n\nVariable flex shank for riding performance and walking comfort\nFull-grain leather\nReflective heel badge for visibility\nElastic lace catch\nNatural gum rubber sole for grip\nLink traction outsole for grip\nTwo-hole cleat compatible\n\n",
                "variant_title": "42",
                "variant_options": [
                  "42"
                ],
                "options_with_values": [
                  {
                    "name": "Size",
                    "value": "42"
                  }
                ],
                "line_level_discount_allocations": [],
                "line_level_total_discount": 0
              }
            ],
            "requires_shipping": true,
            "currency": "HKD",
            "items_subtotal_price": 82700,
            "cart_level_discount_applications": []
          }
        }
        ```

- **CartLoaded**

    ```jsx
    window.addEventListener("Sellify::UCD::CartLoaded", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "cart": {
            "token": "b9983eaec617fee4c98cc8213804ac9d",
            "note": null,
            "attributes": {},
            "original_total_price": 82700,
            "total_price": 82700,
            "total_discount": 0,
            "total_weight": 907.0033,
            "item_count": 1,
            "items": [
              {
                "id": 12543478169683,
                "properties": {

                },
                "quantity": 1,
                "variant_id": 12543478169683,
                "key": "12543478169683:ee62fe287b247705ef707d2a44168db0",
                "title": "DZR Minna - 42",
                "price": 82700,
                "original_price": 82700,
                "discounted_price": 82700,
                "line_price": 82700,
                "original_line_price": 82700,
                "total_discount": 0,
                "discounts": [],
                "sku": "Shoes - DZR - Minna - 42",
                "grams": 907,
                "vendor": "DZR",
                "taxable": true,
                "product_id": 1351134412883,
                "product_has_only_default_variant": false,
                "gift_card": false,
                "final_price": 82700,
                "final_line_price": 82700,
                "url": "/products/dzr-minna?variant=12543478169683",
                "featured_image": {
                  "aspect_ratio": 1.5,
                  "alt": "DZR Minna",
                  "height": 1365,
                  "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                  "width": 2048
                },
                "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                "handle": "dzr-minna",
                "requires_shipping": true,
                "product_type": "Shoes",
                "product_title": "DZR Minna",
                "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesDZR’s all-time best seller, the Minna is proudly named after the gritty S.F. alley their showroom calls home. Understated tones, locally designed graphics, and a Variable Flex Shank combine to create a sneaker that’s as classic in its style as it is comfortable mashing on pedals.\n\nSpecs\n\nVariable flex shank for riding performance and walking comfort\nFull-grain leather\nReflective heel badge for visibility\nElastic lace catch\nNatural gum rubber sole for grip\nLink traction outsole for grip\nTwo-hole cleat compatible\n\n",
                "variant_title": "42",
                "variant_options": [
                  "42"
                ],
                "options_with_values": [
                  {
                    "name": "Size",
                    "value": "42"
                  }
                ],
                "line_level_discount_allocations": [],
                "line_level_total_discount": 0
              }
            ],
            "requires_shipping": true,
            "currency": "HKD",
            "items_subtotal_price": 82700,
            "cart_level_discount_applications": [],
            "paid_items_count": 1
          },
          "show": true
        }
        ```

- **CartBuilt**

    ```jsx
    window.addEventListener("Sellify::UCD::CartBuilt", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "cart": {
            "token": "b9983eaec617fee4c98cc8213804ac9d",
            "note": null,
            "attributes": {},
            "original_total_price": 82700,
            "total_price": 82700,
            "total_discount": 0,
            "total_weight": 907.0033,
            "item_count": 1,
            "items": [
              {
                "id": 12543478169683,
                "properties": {
                  "__ucd": "Upsells"
                },
                "quantity": 1,
                "variant_id": 12543478169683,
                "key": "12543478169683:ee62fe287b247705ef707d2a44168db0",
                "title": "DZR Minna - 42",
                "price": 82700,
                "original_price": 82700,
                "discounted_price": 82700,
                "line_price": 82700,
                "original_line_price": 82700,
                "total_discount": 0,
                "discounts": [],
                "sku": "Shoes - DZR - Minna - 42",
                "grams": 907,
                "vendor": "DZR",
                "taxable": true,
                "product_id": 1351134412883,
                "product_has_only_default_variant": false,
                "gift_card": false,
                "final_price": 82700,
                "final_line_price": 82700,
                "url": "/products/dzr-minna?variant=12543478169683",
                "featured_image": {
                  "aspect_ratio": 1.5,
                  "alt": "DZR Minna",
                  "height": 1365,
                  "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                  "width": 2048
                },
                "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                "handle": "dzr-minna",
                "requires_shipping": true,
                "product_type": "Shoes",
                "product_title": "DZR Minna",
                "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesDZR’s all-time best seller, the Minna is proudly named after the gritty S.F. alley their showroom calls home. Understated tones, locally designed graphics, and a Variable Flex Shank combine to create a sneaker that’s as classic in its style as it is comfortable mashing on pedals.\n\nSpecs\n\nVariable flex shank for riding performance and walking comfort\nFull-grain leather\nReflective heel badge for visibility\nElastic lace catch\nNatural gum rubber sole for grip\nLink traction outsole for grip\nTwo-hole cleat compatible\n\n",
                "variant_title": "42",
                "variant_options": [
                  "42"
                ],
                "options_with_values": [
                  {
                    "name": "Size",
                    "value": "42"
                  }
                ],
                "line_level_discount_allocations": [],
                "line_level_total_discount": 0
              }
            ],
            "requires_shipping": true,
            "currency": "HKD",
            "items_subtotal_price": 82700,
            "cart_level_discount_applications": [],
            "paid_items_count": 1
          }
        }
        ```

- **BeforeTieredFreeItemsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::BeforeTieredFreeItemsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "items": [
            {
              "id": 1351125106771,
              "title": "Club Ride Roxbury Jersey",
              "handle": "roxbury-jersey",
              "body_html": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p class=\"p1\">Once you spend a day in the Roxbury, you'll probably want to spend the night too.  Made with cutting edge RideDryWear, it'll keep you dry on the hottest rides and in the coolest clubs.  The Roxbury also has reflective accents to keep you safe on the road and help you get the attention you deserve off of it.  Couple all that with the Roxbury's rear-pocket media port and you've got a stylish shirt that'll let you keep your tunes bumpin' and your head bobbin' all night long!</p>",
              "published_at": "2018-06-30T03:28:24-04:00",
              "created_at": "2018-06-30T03:21:37-04:00",
              "updated_at": "2018-06-30T03:28:24-04:00",
              "vendor": "Club Ride Appparel",
              "product_type": "Apparel",
              "tags": [
                "Accessories",
                "Apparel",
                "Shirt",
                "Shirts"
              ],
              "variants": [
                {
                  "id": 12543438454867,
                  "title": "S",
                  "option1": "S",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - S",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 70900,
                  "grams": 227,
                  "compare_at_price": null,
                  "position": 1,
                  "product_id": 1351125106771,
                  "created_at": "2018-06-30T03:21:37-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438487635,
                  "title": "M",
                  "option1": "M",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - M",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 70900,
                  "grams": 227,
                  "compare_at_price": null,
                  "position": 2,
                  "product_id": 1351125106771,
                  "created_at": "2018-06-30T03:21:37-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438520403,
                  "title": "L",
                  "option1": "L",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - L",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 70900,
                  "grams": 227,
                  "compare_at_price": null,
                  "position": 3,
                  "product_id": 1351125106771,
                  "created_at": "2018-06-30T03:21:37-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438553171,
                  "title": "XL",
                  "option1": "XL",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - XL",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 70900,
                  "grams": 227,
                  "compare_at_price": null,
                  "position": 4,
                  "product_id": 1351125106771,
                  "created_at": "2018-06-30T03:21:38-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                }
              ],
              "images": [
                {
                  "id": 3816712241235,
                  "created_at": "2018-06-30T03:21:37-04:00",
                  "position": 1,
                  "updated_at": "2018-06-30T03:21:37-04:00",
                  "product_id": 1351125106771,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1530343297",
                  "width": 1200,
                  "height": 800
                }
              ],
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "S",
                    "M",
                    "L",
                    "XL"
                  ]
                }
              ],
              "available_variants_count": 4,
              "url": "/products/roxbury-jersey",
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297",
              "price": "$709.00",
              "price_formatted": "$709.00",
              "compare_at_price": null,
              "compare_at_price_formatted": null,
              "unlocked": true,
              "locked": false,
              "unlock_price": "$300.00",
              "progress": 1414,
              "remaining": -3943
            }
          ],
          "event": "BeforeTieredFreeItemsRendered"
        }
        ```

- **TieredFreeItemsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::TieredFreeItemsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "tiered_free_items": [
            {
              "id": 1351125106771,
              "title": "Club Ride Roxbury Jersey",
              "handle": "roxbury-jersey",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p class=\"p1\">Once you spend a day in the Roxbury, you'll probably want to spend the night too.  Made with cutting edge RideDryWear, it'll keep you dry on the hottest rides and in the coolest clubs.  The Roxbury also has reflective accents to keep you safe on the road and help you get the attention you deserve off of it.  Couple all that with the Roxbury's rear-pocket media port and you've got a stylish shirt that'll let you keep your tunes bumpin' and your head bobbin' all night long!</p>",
              "published_at": "2018-06-30T03:28:24-04:00",
              "created_at": "2018-06-30T03:21:37-04:00",
              "vendor": "Club Ride Appparel",
              "type": "Apparel",
              "tags": [
                "Accessories",
                "Apparel",
                "Shirt",
                "Shirts"
              ],
              "price": "$709.00",
              "price_min": 70900,
              "price_max": 70900,
              "available": true,
              "price_varies": false,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543438454867,
                  "title": "S",
                  "option1": "S",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - S",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - S",
                  "public_title": "S",
                  "options": [
                    "S"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438487635,
                  "title": "M",
                  "option1": "M",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - M",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - M",
                  "public_title": "M",
                  "options": [
                    "M"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438520403,
                  "title": "L",
                  "option1": "L",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - L",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - L",
                  "public_title": "L",
                  "options": [
                    "L"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438553171,
                  "title": "XL",
                  "option1": "XL",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - XL",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - XL",
                  "public_title": "XL",
                  "options": [
                    "XL"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1530343297"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1530343297",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "S",
                    "M",
                    "L",
                    "XL"
                  ]
                }
              ],
              "url": "/products/roxbury-jersey",
              "media": [
                {
                  "alt": null,
                  "id": 1379425026131,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1569177889",
                  "width": 1200
                }
              ],
              "available_variants_count": 4,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297",
              "price_formatted": "$709.00",
              "compare_at_price_formatted": null,
              "unlocked": true,
              "locked": false,
              "unlock_price": "$300.00",
              "progress": 1414,
              "remaining": -3943
            }
          ],
          "event": "TieredFreeItemsRendered"
        }
        ```

- **CartHidden**

    ```jsx
    window.addEventListener("Sellify::UCD::CartHidden", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
        }
        ```

- **CartVisible**

    ```jsx
    window.addEventListener("Sellify::UCD::CartVisible", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
        }
        ```

- **ItemAdded**

    ```jsx
    window.addEventListener("Sellify::UCD::ItemAdded", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "line_item": {
            "id": 12543449890899,
            "properties": null,
            "quantity": 1,
            "variant_id": 12543449890899,
            "key": "12543449890899:6ed6ba3a3d7700eaa1af6db92d823c0f",
            "title": "Whiskey - 50 cm",
            "price": 258900,
            "original_price": 258900,
            "discounted_price": 258900,
            "line_price": 258900,
            "original_line_price": 258900,
            "total_discount": 0,
            "discounts": [],
            "sku": "The Whiskey - Small",
            "grams": 28123,
            "vendor": "Pure Fix Cycles",
            "taxable": true,
            "product_id": 1351127826515,
            "product_has_only_default_variant": false,
            "gift_card": false,
            "final_price": 258900,
            "final_line_price": 258900,
            "url": "/products/whiskey-grey-blue-fixie?variant=12543449890899",
            "featured_image": {
              "aspect_ratio": 1.5,
              "alt": "Whiskey",
              "height": 1365,
              "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/WHISKEY_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892",
              "width": 2048
            },
            "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/WHISKEY_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892",
            "handle": "whiskey-grey-blue-fixie",
            "requires_shipping": true,
            "product_type": "Fixed Gear Bicycle",
            "product_title": "Whiskey",
            "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesIf the Whiskey were a beverage, it would definitely be a 12-year-old Scotch. Blue on grey for a smoky, timeless style.",
            "variant_title": "50 cm",
            "variant_options": [
              "50 cm"
            ],
            "options_with_values": [
              {
                "name": "Size",
                "value": "50 cm"
              }
            ],
            "line_level_discount_allocations": [],
            "line_level_total_discount": 0
          },
          "form": {
            "0": {
              "0": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "1": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "2": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "jQuery223052251611631823262": {
                "index": "option1"
              },
              "jQuery223052251611631823261": {
                "events": {
                  "change": [
                    {
                      "type": "change",
                      "origType": "change",
                      "guid": 14,
                      "namespace": ""
                    },
                    {
                      "type": "change",
                      "origType": "change",
                      "data": null,
                      "guid": 73,
                      "namespace": "single-option-selector"
                    }
                  ],
                  "click": [
                    {
                      "type": "click",
                      "origType": "click",
                      "data": null,
                      "guid": 74,
                      "namespace": ""
                    }
                  ],
                  "touchend": [
                    {
                      "type": "touchend",
                      "origType": "touchend",
                      "guid": 78,
                      "namespace": "removePriceTooltipOnHover"
                    }
                  ]
                }
              }
            },
            "1": {
              "0": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "1": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "2": {
                "jQuery223052251611631823261": {
                  "events": {
                    "touchend": [
                      {
                        "type": "touchend",
                        "origType": "touchend",
                        "guid": 78,
                        "namespace": "removePriceTooltipOnHover"
                      }
                    ]
                  }
                }
              },
              "jQuery223052251611631823261": {
                "events": {
                  "click": [
                    {
                      "type": "click",
                      "origType": "click",
                      "data": null,
                      "guid": 74,
                      "namespace": ""
                    }
                  ],
                  "touchend": [
                    {
                      "type": "touchend",
                      "origType": "touchend",
                      "guid": 78,
                      "namespace": "removePriceTooltipOnHover"
                    }
                  ]
                }
              }
            },
            "2": {
              "jQuery223052251611631823261": {
                "events": {
                  "touchend": [
                    {
                      "type": "touchend",
                      "origType": "touchend",
                      "guid": 78,
                      "namespace": "removePriceTooltipOnHover"
                    }
                  ]
                }
              },
              "sizzle1590754599524": {
                "undefined": {
                  "parentNode": [
                    84,
                    29,
                    false
                  ]
                }
              }
            },
            "jQuery223052251611631823261": {
              "events": {
                "submit": [
                  {
                    "type": "submit",
                    "origType": "submit",
                    "data": null,
                    "guid": 66,
                    "namespace": ""
                  }
                ],
                "change": [
                  {
                    "type": "change",
                    "origType": "change",
                    "data": null,
                    "guid": 67,
                    "namespace": ""
                  }
                ],
                "touchend": [
                  {
                    "type": "touchend",
                    "origType": "touchend",
                    "guid": 78,
                    "namespace": "removePriceTooltipOnHover"
                  }
                ]
              }
            },
            "sizzle1590754598892": {
              "undefined": {
                "parentNode": [
                  67,
                  3,
                  true
                ]
              }
            },
            "sizzle1590754599524": {
              "undefined": {
                "parentNode": [
                  96,
                  29,
                  false
                ]
              }
            }
          },
          "event": "ItemAdded"
        }
        ```

- **BeforeUpsellsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::BeforeUpsellsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "items": [
            {
              "id": 1351134380115,
              "title": "DZR Mechanic",
              "handle": "dzr-mechanic",
              "body_html": "This is a demonstration store.",
              "published_at": "2018-06-30T03:33:59-04:00",
              "created_at": "2018-06-30T03:34:00-04:00",
              "updated_at": "2018-06-30T03:34:00-04:00",
              "vendor": "DZR",
              "product_type": "Shoes",
              "tags": [
                "Accessories",
                "Apparel",
                "Shoes"
              ],
              "variants": [
                {
                  "id": 12543477973075,
                  "title": "41",
                  "option1": "41",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mechanic - 41",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 78000,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 1,
                  "product_id": 1351134380115,
                  "created_at": "2018-06-30T03:34:00-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$780.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MECHANIC_PAIR_FRONT_WEB_large.jpg?v=1530344040"
                },
                {
                  "id": 12543478104147,
                  "title": "45",
                  "option1": "45",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mechanic - 45",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 78000,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 5,
                  "product_id": 1351134380115,
                  "created_at": "2018-06-30T03:34:00-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$780.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MECHANIC_PAIR_FRONT_WEB_large.jpg?v=1530344040"
                }
              ],
              "images": [
                {
                  "id": 3816806875219,
                  "created_at": "2018-06-30T03:34:00-04:00",
                  "position": 1,
                  "updated_at": "2018-06-30T03:34:00-04:00",
                  "product_id": 1351134380115,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MECHANIC_PAIR_FRONT_WEB.jpg?v=1530344040",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806907987,
                  "created_at": "2018-06-30T03:34:00-04:00",
                  "position": 2,
                  "updated_at": "2018-06-30T03:34:00-04:00",
                  "product_id": 1351134380115,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MECHANIC_PAIR_BACK_WEB.jpg?v=1530344040",
                  "width": 2048,
                  "height": 1365
                }
              ],
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "41",
                    "42",
                    "43",
                    "44",
                    "45"
                  ]
                }
              ],
              "available_variants_count": 2,
              "url": "/products/dzr-mechanic",
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MECHANIC_PAIR_FRONT_WEB_large.jpg?v=1530344040",
              "price": "$780.00",
              "price_formatted": "$780.00",
              "compare_at_price": null,
              "compare_at_price_formatted": null
            },
            {
              "id": 1351134347347,
              "title": "DZR Mamba",
              "handle": "dzr-mamba",
              "body_html": "This is a demonstration store.",
              "published_at": "2018-06-30T03:33:57-04:00",
              "created_at": "2018-06-30T03:33:58-04:00",
              "updated_at": "2018-06-30T03:33:59-04:00",
              "vendor": "DZR",
              "product_type": "Shoes",
              "tags": [
                "Accessories",
                "Apparel",
                "Shoes"
              ],
              "variants": [
                {
                  "id": 12543477809235,
                  "title": "41",
                  "option1": "41",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mamba Black - 41",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 94500,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 1,
                  "product_id": 1351134347347,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$945.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038"
                },
                {
                  "id": 12543477842003,
                  "title": "42",
                  "option1": "42",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mamba Black - 42",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 94500,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 2,
                  "product_id": 1351134347347,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$945.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038"
                },
                {
                  "id": 12543477874771,
                  "title": "43",
                  "option1": "43",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mamba Black - 43",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 94500,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 3,
                  "product_id": 1351134347347,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$945.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038"
                },
                {
                  "id": 12543477907539,
                  "title": "44",
                  "option1": "44",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mamba Black - 44",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 94500,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 4,
                  "product_id": 1351134347347,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$945.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038"
                },
                {
                  "id": 12543477940307,
                  "title": "45",
                  "option1": "45",
                  "option2": null,
                  "option3": null,
                  "sku": "Shoes - DZR - Mamba Black - 45",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "price": 94500,
                  "grams": 907,
                  "compare_at_price": null,
                  "position": 5,
                  "product_id": 1351134347347,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$945.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038"
                }
              ],
              "images": [
                {
                  "id": 3816806809683,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "position": 1,
                  "updated_at": "2018-06-30T03:33:58-04:00",
                  "product_id": 1351134347347,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB.jpg?v=1530344038",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806842451,
                  "created_at": "2018-06-30T03:33:58-04:00",
                  "position": 2,
                  "updated_at": "2018-06-30T03:33:58-04:00",
                  "product_id": 1351134347347,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_BACK_WEB.jpg?v=1530344038",
                  "width": 2048,
                  "height": 1365
                }
              ],
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "41",
                    "42",
                    "43",
                    "44",
                    "45"
                  ]
                }
              ],
              "available_variants_count": 5,
              "url": "/products/dzr-mamba",
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MAMBA_PAIR_FRONT_WEB_large.jpg?v=1530344038",
              "price": "$945.00",
              "price_formatted": "$945.00",
              "compare_at_price": null,
              "compare_at_price_formatted": null
            },
            {
              "id": 1351134314579,
              "title": "Factory 5 Lattice Chainring - 49T",
              "handle": "factory-5-lattice-chainring-49t",
              "body_html": "This is a demonstration store.",
              "published_at": "2018-06-30T03:33:55-04:00",
              "created_at": "2018-06-30T03:33:56-04:00",
              "updated_at": "2018-06-30T03:33:56-04:00",
              "vendor": "Factory 5",
              "product_type": "Chainrings",
              "tags": [
                "Chainrings",
                "Drivetrain",
                "Parts"
              ],
              "variants": [
                {
                  "id": 12543477743699,
                  "title": "Black",
                  "option1": "Black",
                  "option2": null,
                  "option3": null,
                  "sku": "Chainring - F5 Lattice - 49T Black",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816806678611,
                    "product_id": 1351134314579,
                    "position": 2,
                    "created_at": "2018-06-30T03:33:56-04:00",
                    "updated_at": "2018-06-30T03:33:56-04:00",
                    "alt": null,
                    "width": 2048,
                    "height": 1365,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_BLACK_WEB.jpg?v=1530344036",
                    "variant_ids": [
                      12543477743699
                    ]
                  },
                  "available": true,
                  "price": 70900,
                  "grams": 0,
                  "compare_at_price": null,
                  "position": 1,
                  "product_id": 1351134314579,
                  "created_at": "2018-06-30T03:33:56-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_BLACK_WEB_large.jpg?v=1530344036"
                },
                {
                  "id": 12543477776467,
                  "title": "Silver",
                  "option1": "Silver",
                  "option2": null,
                  "option3": null,
                  "sku": "Chainring - F5 Lattice - 49T Silver",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816806711379,
                    "product_id": 1351134314579,
                    "position": 3,
                    "created_at": "2018-06-30T03:33:56-04:00",
                    "updated_at": "2018-06-30T03:33:56-04:00",
                    "alt": null,
                    "width": 2048,
                    "height": 1365,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_49T-SILVER_WEB.jpg?v=1530344036",
                    "variant_ids": [
                      12543477776467
                    ]
                  },
                  "available": true,
                  "price": 70900,
                  "grams": 0,
                  "compare_at_price": null,
                  "position": 2,
                  "product_id": 1351134314579,
                  "created_at": "2018-06-30T03:33:56-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$709.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_49T-SILVER_WEB_large.jpg?v=1530344036"
                }
              ],
              "images": [
                {
                  "id": 3816806645843,
                  "created_at": "2018-06-30T03:33:56-04:00",
                  "position": 1,
                  "updated_at": "2018-06-30T03:33:56-04:00",
                  "product_id": 1351134314579,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_BLACK-N-SILVER_FRONT_WEB.jpg?v=1530344036",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806678611,
                  "created_at": "2018-06-30T03:33:56-04:00",
                  "position": 2,
                  "updated_at": "2018-06-30T03:33:56-04:00",
                  "product_id": 1351134314579,
                  "variant_ids": [
                    12543477743699
                  ],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_BLACK_WEB.jpg?v=1530344036",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806711379,
                  "created_at": "2018-06-30T03:33:56-04:00",
                  "position": 3,
                  "updated_at": "2018-06-30T03:33:56-04:00",
                  "product_id": 1351134314579,
                  "variant_ids": [
                    12543477776467
                  ],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_49T-SILVER_WEB.jpg?v=1530344036",
                  "width": 2048,
                  "height": 1365
                }
              ],
              "options": [
                {
                  "name": "Color",
                  "position": 1,
                  "values": [
                    "Black",
                    "Silver"
                  ]
                }
              ],
              "available_variants_count": 2,
              "url": "/products/factory-5-lattice-chainring-49t",
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/CHAINRING_F5-LATTICE_BLACK-N-SILVER_FRONT_WEB_large.jpg?v=1530344036",
              "price": "$709.00",
              "price_formatted": "$709.00",
              "compare_at_price": null,
              "compare_at_price_formatted": null
            },
            {
              "id": 1351134249043,
              "title": "Dalman Supply Co. Rope Locks",
              "handle": "dalman-supply-co-rope-locks",
              "body_html": "This is a demonstration store.",
              "published_at": "2018-06-30T03:33:51-04:00",
              "created_at": "2018-06-30T03:33:52-04:00",
              "updated_at": "2018-06-30T03:33:53-04:00",
              "vendor": "Dalman Supply Co.",
              "product_type": "Locks",
              "tags": [
                "Accessories",
                "Locks"
              ],
              "variants": [
                {
                  "id": 12543477579859,
                  "title": "26\"",
                  "option1": "26\"",
                  "option2": null,
                  "option3": null,
                  "sku": "Lock - Dalman - 26\" Natural Cab",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816806449235,
                    "product_id": 1351134249043,
                    "position": 2,
                    "created_at": "2018-06-30T03:33:53-04:00",
                    "updated_at": "2018-06-30T03:33:53-04:00",
                    "alt": null,
                    "width": 2048,
                    "height": 1365,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_5FT_LONG-JON_COILED_WEB.jpg?v=1530344033",
                    "variant_ids": [
                      12543477579859
                    ]
                  },
                  "available": true,
                  "price": 23700,
                  "grams": 1134,
                  "compare_at_price": null,
                  "position": 1,
                  "product_id": 1351134249043,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$237.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_5FT_LONG-JON_COILED_WEB_large.jpg?v=1530344033"
                },
                {
                  "id": 12543477612627,
                  "title": "60\"",
                  "option1": "60\"",
                  "option2": null,
                  "option3": null,
                  "sku": "Lock - Dalman - 5' Long Jon",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816806482003,
                    "product_id": 1351134249043,
                    "position": 3,
                    "created_at": "2018-06-30T03:33:53-04:00",
                    "updated_at": "2018-06-30T03:33:53-04:00",
                    "alt": null,
                    "width": 2048,
                    "height": 1365,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_26IN_NATURAL-CAB_COILED_WEB.jpg?v=1530344033",
                    "variant_ids": [
                      12543477612627
                    ]
                  },
                  "available": true,
                  "price": 39400,
                  "grams": 1134,
                  "compare_at_price": null,
                  "position": 2,
                  "product_id": 1351134249043,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "updated_at": "2018-09-12T01:41:21-04:00",
                  "price_formatted": "$394.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_26IN_NATURAL-CAB_COILED_WEB_large.jpg?v=1530344033"
                }
              ],
              "images": [
                {
                  "id": 3816806416467,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "position": 1,
                  "updated_at": "2018-06-30T03:33:53-04:00",
                  "product_id": 1351134249043,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_26IN-AND-5IN_SET_WEB.jpg?v=1530344033",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806449235,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "position": 2,
                  "updated_at": "2018-06-30T03:33:53-04:00",
                  "product_id": 1351134249043,
                  "variant_ids": [
                    12543477579859
                  ],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_5FT_LONG-JON_COILED_WEB.jpg?v=1530344033",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806482003,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "position": 3,
                  "updated_at": "2018-06-30T03:33:53-04:00",
                  "product_id": 1351134249043,
                  "variant_ids": [
                    12543477612627
                  ],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_26IN_NATURAL-CAB_COILED_WEB.jpg?v=1530344033",
                  "width": 2048,
                  "height": 1365
                },
                {
                  "id": 3816806514771,
                  "created_at": "2018-06-30T03:33:53-04:00",
                  "position": 4,
                  "updated_at": "2018-06-30T03:33:53-04:00",
                  "product_id": 1351134249043,
                  "variant_ids": [],
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_5FT_LONG-JON_OPEN_WEB.jpg?v=1530344033",
                  "width": 2048,
                  "height": 1365
                }
              ],
              "options": [
                {
                  "name": "Length",
                  "position": 1,
                  "values": [
                    "26\"",
                    "60\""
                  ]
                }
              ],
              "available_variants_count": 2,
              "url": "/products/dalman-supply-co-rope-locks",
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/DALMAN-LOCK_26IN-AND-5IN_SET_WEB_large.jpg?v=1530344033",
              "price": "$237.00",
              "price_formatted": "$237.00",
              "compare_at_price": null,
              "compare_at_price_formatted": null
            }
          ],
          "event": "BeforeUpsellsRendered"
        }
        ```

- **UpsellsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::UpsellsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "upsells": [
            {
              "id": 1351125106771,
              "title": "Club Ride Roxbury Jersey",
              "handle": "roxbury-jersey",
              "description": "This is a demonstration store.",
              "published_at": "2018-06-30T03:28:24-04:00",
              "created_at": "2018-06-30T03:21:37-04:00",
              "vendor": "Club Ride Appparel",
              "type": "Apparel",
              "tags": [
                "Accessories",
                "Apparel",
                "Shirt",
                "Shirts"
              ],
              "price": "$709.00",
              "price_min": 70900,
              "price_max": 70900,
              "available": true,
              "price_varies": false,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543438454867,
                  "title": "S",
                  "option1": "S",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - S",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - S",
                  "public_title": "S",
                  "options": [
                    "S"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438487635,
                  "title": "M",
                  "option1": "M",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - M",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - M",
                  "public_title": "M",
                  "options": [
                    "M"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438520403,
                  "title": "L",
                  "option1": "L",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - L",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - L",
                  "public_title": "L",
                  "options": [
                    "L"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                },
                {
                  "id": 12543438553171,
                  "title": "XL",
                  "option1": "XL",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Roxbury - Char - XL",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Roxbury Jersey - XL",
                  "public_title": "XL",
                  "options": [
                    "XL"
                  ],
                  "price": 70900,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$709.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1530343297"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1530343297",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "S",
                    "M",
                    "L",
                    "XL"
                  ]
                }
              ],
              "url": "/products/roxbury-jersey",
              "media": [
                {
                  "alt": null,
                  "id": 1379425026131,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal.jpg?v=1569177889",
                  "width": 1200
                }
              ],
              "available_variants_count": 4,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/roxbury-charcoal_large.jpg?v=1530343297",
              "price_formatted": "$709.00",
              "compare_at_price_formatted": null
            }
          ],
          "event": "UpsellsRendered"
        }
        ```

- **BeforeRecommendedProductsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::BeforeRecommendedProductsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "items": [
            {
              "id": 1351129989203,
              "title": "650C 45mm Micro Wheelset",
              "handle": "650c-micro-wheelset",
              "description": "This is a demonstration store.",
              "published_at": "2018-06-30T03:27:39-04:00",
              "created_at": "2018-06-30T03:27:41-04:00",
              "vendor": "Pure Fix Cycles",
              "type": "Wheelsets",
              "tags": [
                "650C",
                "650C Wheelsets",
                "Black",
                "Blue",
                "Micro",
                "Orange",
                "Wheels",
                "Wheelset",
                "Wheelsets and Accessories",
                "White"
              ],
              "price": "$1,023.00",
              "price_min": 102300,
              "price_max": 102300,
              "available": true,
              "price_varies": false,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543456673875,
                  "title": "Orange",
                  "option1": "Orange",
                  "option2": null,
                  "option3": null,
                  "sku": "Orange Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816759951443,
                    "product_id": 1351129989203,
                    "position": 1,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "Orange",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456673875
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - Orange",
                  "public_title": "Orange",
                  "options": [
                    "Orange"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638785",
                  "featured_media": {
                    "alt": "Orange",
                    "id": 1379442163795,
                    "position": 1,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web_large.jpg?v=1530343662"
                },
                {
                  "id": 12543456706643,
                  "title": "Black",
                  "option1": "Black",
                  "option2": null,
                  "option3": null,
                  "sku": "Black Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816759984211,
                    "product_id": 1351129989203,
                    "position": 2,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "Black",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456706643
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - Black",
                  "public_title": "Black",
                  "options": [
                    "Black"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638761",
                  "featured_media": {
                    "alt": "Black",
                    "id": 1379442196563,
                    "position": 2,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web_large.jpg?v=1530343662"
                },
                {
                  "id": 12543456772179,
                  "title": "White",
                  "option1": "White",
                  "option2": null,
                  "option3": null,
                  "sku": "White Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816760049747,
                    "product_id": 1351129989203,
                    "position": 4,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "White",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456772179
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - White",
                  "public_title": "White",
                  "options": [
                    "White"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638778",
                  "featured_media": {
                    "alt": "White",
                    "id": 1379442262099,
                    "position": 4,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web_large.jpg?v=1530343662"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1530343662"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
              "options": [
                {
                  "name": "Color",
                  "position": 1,
                  "values": [
                    "Orange",
                    "Black",
                    "Blue",
                    "White"
                  ]
                }
              ],
              "url": "/products/650c-micro-wheelset?pr_prod_strat=collection_fallback&pr_rec_pid=1351129989203&pr_ref_pid=1351134412883&pr_seq=uniform",
              "media": [
                {
                  "alt": "Orange",
                  "id": 1379442163795,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "Black",
                  "id": 1379442196563,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "Blue",
                  "id": 1379442229331,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "White",
                  "id": 1379442262099,
                  "position": 4,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893",
                  "width": 1200
                }
              ],
              "available_variants_count": 3,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web_large.jpg?v=1530343662",
              "price_formatted": "$1,023.00",
              "compare_at_price_formatted": null
            }
          ],
          "event": "BeforeRecommendedProductsRendered"
        }
        ```

- **RecommendedProductsRendered**

    ```jsx
    window.addEventListener("Sellify::UCD::RecommendedProductsRendered", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "recommended_products": [
            {
              "id": 1351129989203,
              "title": "650C 45mm Micro Wheelset",
              "handle": "650c-micro-wheelset",
        	      "description": "This is a demonstration store.",
              "published_at": "2018-06-30T03:27:39-04:00",
              "created_at": "2018-06-30T03:27:41-04:00",
              "vendor": "Pure Fix Cycles",
              "type": "Wheelsets",
              "tags": [
                "650C",
                "650C Wheelsets",
                "Black",
                "Blue",
                "Micro",
                "Orange",
                "Wheels",
                "Wheelset",
                "Wheelsets and Accessories",
                "White"
              ],
              "price": "$1,023.00",
              "price_min": 102300,
              "price_max": 102300,
              "available": true,
              "price_varies": false,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543456673875,
                  "title": "Orange",
                  "option1": "Orange",
                  "option2": null,
                  "option3": null,
                  "sku": "Orange Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816759951443,
                    "product_id": 1351129989203,
                    "position": 1,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "Orange",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456673875
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - Orange",
                  "public_title": "Orange",
                  "options": [
                    "Orange"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638785",
                  "featured_media": {
                    "alt": "Orange",
                    "id": 1379442163795,
                    "position": 1,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web_large.jpg?v=1530343662"
                },
                {
                  "id": 12543456706643,
                  "title": "Black",
                  "option1": "Black",
                  "option2": null,
                  "option3": null,
                  "sku": "Black Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816759984211,
                    "product_id": 1351129989203,
                    "position": 2,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "Black",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456706643
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - Black",
                  "public_title": "Black",
                  "options": [
                    "Black"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638761",
                  "featured_media": {
                    "alt": "Black",
                    "id": 1379442196563,
                    "position": 2,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web_large.jpg?v=1530343662"
                },
                {
                  "id": 12543456772179,
                  "title": "White",
                  "option1": "White",
                  "option2": null,
                  "option3": null,
                  "sku": "White Wheels 650c",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": {
                    "id": 3816760049747,
                    "product_id": 1351129989203,
                    "position": 4,
                    "created_at": "2018-06-30T03:27:41-04:00",
                    "updated_at": "2018-06-30T03:27:42-04:00",
                    "alt": "White",
                    "width": 1200,
                    "height": 800,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1530343662",
                    "variant_ids": [
                      12543456772179
                    ]
                  },
                  "available": true,
                  "name": "650C 45mm Micro Wheelset - White",
                  "public_title": "White",
                  "options": [
                    "White"
                  ],
                  "price": 102300,
                  "weight": 13608,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360638778",
                  "featured_media": {
                    "alt": "White",
                    "id": 1379442262099,
                    "position": 4,
                    "preview_image": {
                      "aspect_ratio": 1.5,
                      "height": 800,
                      "width": 1200,
                      "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893"
                    }
                  },
                  "price_formatted": "$1,023.00",
                  "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web_large.jpg?v=1530343662"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1530343662",
                "//cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1530343662"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1530343662",
              "options": [
                {
                  "name": "Color",
                  "position": 1,
                  "values": [
                    "Orange",
                    "Black",
                    "Blue",
                    "White"
                  ]
                }
              ],
              "url": "/products/650c-micro-wheelset?pr_prod_strat=collection_fallback&pr_rec_pid=1351129989203&pr_ref_pid=1351134412883&pr_seq=uniform",
              "media": [
                {
                  "alt": "Orange",
                  "id": 1379442163795,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "Black",
                  "id": 1379442196563,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_black_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "Blue",
                  "id": 1379442229331,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_blue_web.jpg?v=1569177893",
                  "width": 1200
                },
                {
                  "alt": "White",
                  "id": 1379442262099,
                  "position": 4,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/650_white_web.jpg?v=1569177893",
                  "width": 1200
                }
              ],
              "available_variants_count": 3,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/650_orange_web_large.jpg?v=1530343662",
              "price_formatted": "$1,023.00",
              "compare_at_price_formatted": null
            }
          ],
          "event": "RecommendedProductsRendered"
        }
        ```

- **CartUpdated**

    ```jsx
    window.addEventListener("Sellify::UCD::CartUpdated", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
          "cart": {
            "token": "b9983eaec617fee4c98cc8213804ac9d",
            "note": null,
            "attributes": {},
            "original_total_price": 165400,
            "total_price": 165400,
            "total_discount": 0,
            "total_weight": 1814.0066,
            "item_count": 2,
            "items": [
              {
                "id": 12543478169683,
                "properties": {
                  "__ucd": "Upsells"
                },
                "quantity": 2,
                "variant_id": 12543478169683,
                "key": "12543478169683:ee62fe287b247705ef707d2a44168db0",
                "title": "DZR Minna - 42",
                "price": 82700,
                "original_price": 82700,
                "discounted_price": 82700,
                "line_price": 165400,
                "original_line_price": 165400,
                "total_discount": 0,
                "discounts": [],
                "sku": "Shoes - DZR - Minna - 42",
                "grams": 907,
                "vendor": "DZR",
                "taxable": true,
                "product_id": 1351134412883,
                "product_has_only_default_variant": false,
                "gift_card": false,
                "final_price": 82700,
                "final_line_price": 165400,
                "url": "/products/dzr-minna?variant=12543478169683",
                "featured_image": {
                  "aspect_ratio": 1.5,
                  "alt": "DZR Minna",
                  "height": 1365,
                  "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                  "width": 2048
                },
                "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                "handle": "dzr-minna",
                "requires_shipping": true,
                "product_type": "Shoes",
                "product_title": "DZR Minna",
                "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesDZR’s all-time best seller, the Minna is proudly named after the gritty S.F. alley their showroom calls home. Understated tones, locally designed graphics, and a Variable Flex Shank combine to create a sneaker that’s as classic in its style as it is comfortable mashing on pedals.\n\nSpecs\n\nVariable flex shank for riding performance and walking comfort\nFull-grain leather\nReflective heel badge for visibility\nElastic lace catch\nNatural gum rubber sole for grip\nLink traction outsole for grip\nTwo-hole cleat compatible\n\n",
                "variant_title": "42",
                "variant_options": [
                  "42"
                ],
                "options_with_values": [
                  {
                    "name": "Size",
                    "value": "42"
                  }
                ],
                "line_level_discount_allocations": [],
                "line_level_total_discount": 0
              }
            ],
            "requires_shipping": true,
            "currency": "HKD",
            "items_subtotal_price": 165400,
            "cart_level_discount_applications": []
          },
          "updates": {
            "updates": {
              "12543478169683:ee62fe287b247705ef707d2a44168db0": 2
            }
          },
          "previous_cart": {
            "token": "b9983eaec617fee4c98cc8213804ac9d",
            "note": null,
            "attributes": {},
            "original_total_price": 82700,
            "total_price": 82700,
            "total_discount": 0,
            "total_weight": 907.0033,
            "item_count": 1,
            "items": [
              {
                "id": 12543478169683,
                "properties": {
                  "__ucd": "Upsells"
                },
                "quantity": 1,
                "variant_id": 12543478169683,
                "key": "12543478169683:ee62fe287b247705ef707d2a44168db0",
                "title": "DZR Minna - 42",
                "price": 82700,
                "original_price": 82700,
                "discounted_price": 82700,
                "line_price": 82700,
                "original_line_price": 82700,
                "total_discount": 0,
                "discounts": [],
                "sku": "Shoes - DZR - Minna - 42",
                "grams": 907,
                "vendor": "DZR",
                "taxable": true,
                "product_id": 1351134412883,
                "product_has_only_default_variant": false,
                "gift_card": false,
                "final_price": 82700,
                "final_line_price": 82700,
                "url": "/products/dzr-minna?variant=12543478169683",
                "featured_image": {
                  "aspect_ratio": 1.5,
                  "alt": "DZR Minna",
                  "height": 1365,
                  "url": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                  "width": 2048
                },
                "image": "https://cdn.shopify.com/s/files/1/2325/8929/products/DZR_MINNA_PAIR_FRONT_WEB.jpg?v=1569177897",
                "handle": "dzr-minna",
                "requires_shipping": true,
                "product_type": "Shoes",
                "product_title": "DZR Minna",
                "product_description": "This is a demonstration store. You can purchase products like this from Pure Fix CyclesDZR’s all-time best seller, the Minna is proudly named after the gritty S.F. alley their showroom calls home. Understated tones, locally designed graphics, and a Variable Flex Shank combine to create a sneaker that’s as classic in its style as it is comfortable mashing on pedals.\n\nSpecs\n\nVariable flex shank for riding performance and walking comfort\nFull-grain leather\nReflective heel badge for visibility\nElastic lace catch\nNatural gum rubber sole for grip\nLink traction outsole for grip\nTwo-hole cleat compatible\n\n",
                "variant_title": "42",
                "variant_options": [
                  "42"
                ],
                "options_with_values": [
                  {
                    "name": "Size",
                    "value": "42"
                  }
                ],
                "line_level_discount_allocations": [],
                "line_level_total_discount": 0
              }
            ],
            "requires_shipping": true,
            "currency": "HKD",
            "items_subtotal_price": 82700,
            "cart_level_discount_applications": [],
            "paid_items_count": 1
          },
          "event": "CartUpdated"
        }
        ```

- **ConvertPrices**

    This event is dispatched when your currency app need to convert prices.

    ```jsx
    window.addEventListener("ConvertPrices", function(e){
      console.log(e.detail);
    });
    ```

    - Toggle event detail `e.detail`

        ```json
        {
        }
        ```

If you want a currency conversion app which has automatic integration with ULTIMATE Cart Drawer, Check our very own currency conversion app: [https://apps.shopify.com/ultimate-currency-converter](https://apps.shopify.com/ultimate-currency-converter)