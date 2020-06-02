# Theme variables Reference

1. Cart

    Use the following code snippet in console of the browser where home page of your store is open and it will log all the actual variables available for your store:

    ```jsx
    sellify.ucd.filters.cart_final.push(function(cart){
    	console.log(cart)
    });
    ```

    - Toggle sample variables

        ```json
        {
          "special_offer_notification": "",
          "remaining_amount": "",
          "translations": {
            "cart": {
              "review_your_cart": "Review your cart",
              "remove": "Remove",
              "subtotal": "Subtotal",
              "discount": "Discount",
              "total": "Total",
              "special_instructions_for_seller": "Special instructions for seller",
              "checkout": "Checkout",
              "empty_cart": "Your cart is currently empty.",
              "continue_shopping": "Continue Shopping"
            },
            "special_offers": {
              "notification_1_qualified": "CONGRATULATIONS, YOU'VE QUALIFIED FOR FREE SHIPPING.",
              "notification_1_unqualified": "ALMOST THERE, ADD {{remaining_amount}} MORE TO GET FREE SHIPPING."
            },
            "discount_code": {
              "apply": "Apply",
              "discount": "Discount",
              "placeholder": "eg. DISCOUNT CODE",
              "fallback_error_message": "Something went wrong!"
            },
            "upsells": {
              "title": "YOU MIGHT ALSO LIKE THESE",
              "add": "Add"
            },
            "tiered_free_items": {
              "title": "",
              "add": "Add",
              "unlock_at": "Unlock at"
            },
            "recommended_products": {
              "title": "FREQUENTLY BOUGHT WITH",
              "add": "Add"
            }
          },
          "upsells_title": "YOU MIGHT ALSO LIKE THESE:",
          "tiered_free_items_title": "[Shopify Plus Only] UNLOCK A FREE GIFT",
          "recommended_products_title": "FREQUENTLY BOUGHT TOGETHER:",
          "recommended_products": "",
          "token": "b9983eaec617fee4c98cc8213804ac9d",
          "note": "",
          "attributes": {},
          "original_total_price": 258900,
          "total_price": 258900,
          "total_discount": 0,
          "total_weight": 28122.9991,
          "item_count": 1,
          "items": [
            {
              "id": 12543449890899,
              "properties": {},
              "quantity": 1,
              "variant_id": 12543449890899,
              "key": "12543449890899:6ed6ba3a3d7700eaa1af6db92d823c0f",
              "title": "Whiskey - 50 cm",
              "price": "$2,589.00",
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
              "line_level_total_discount": 0,
              "line": 1,
              "img": "https://cdn.shopify.com/s/files/1/2325/8929/products/WHISKEY_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1569177892",
              "name": "Whiskey",
              "variation": "50 cm",
              "original_properties": {},
              "itemAdd": 2,
              "itemMinus": 0,
              "itemQty": 1,
              "price_formatted": "$2,589.00",
              "original_price_formatted": "$2,589.00",
              "discounted_price_formatted": "$2,589.00",
              "linePrice": "$2,589.00",
              "line_price_formatted": "$2,589.00",
              "original_line_price_formatted": "$2,589.00",
              "total_discount_formatted": "$0.00",
              "final_price_formatted": "$2,589.00",
              "final_line_price_formatted": "$2,589.00",
              "originalPrice": "$2,589.00",
              "discountsApplied": false
            }
          ],
          "requires_shipping": true,
          "currency": "HKD",
          "items_subtotal_price": 258900,
          "cart_level_discount_applications": [],
          "paid_items_count": 1,
          "totalPrice": "$2,589.00",
          "total_price_formatted": "$2,589.00",
          "original_total_price_formatted": "$2,589.00",
          "items_subtotal_price_formatted": "$2,589.00",
          "totalCartDiscount": 0,
          "total_discount_formatted": 0,
          "totalCartDiscountApplied": false,
          "special_offers": {
            "tiers": [
              {
                "message": "CONGRATULATIONS, YOU'VE QUALIFIED FOR FREE SHIPPING.",
                "value": 300,
                "progress": 100,
                "remaining_amount": 0,
                "remaining": 0,
                "qualified": true
              }
            ],
            "progress": 100,
            "show_progress_bar": true,
            "progress_tier": {
              "message": "CONGRATULATIONS, YOU'VE QUALIFIED FOR FREE SHIPPING.",
              "value": 300,
              "progress": 100,
              "remaining_amount": 0,
              "remaining": 0,
              "qualified": true
            }
          }
        }
        ```

2. Automatic Products Recommendations

    ```jsx
    sellify.ucd.filters.recommended_products.push(function(products){
    	console.log({recommended_products: products});
    });
    ```

    - Toggle sample variables

        ```json
        {
          "recommended_products": [
            {
              "id": 1351125074003,
              "title": "Club Ride Ray Jean",
              "handle": "ray-jean",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p class=\"p1\">\"You rode here in jeans?!\" Your envious friends gasp, \"Aren't they heavy?\" Not these. The Ray Jean was designed specifically for riders who like the comfort of bike-wear without all the spandex and sideways glances it causes once you're away from your ride. The Ray Jean is made with StretchRide2 (the better-than-the-original sequel to StretchRide) and is 30% lighter than standard denim. It breathes well in warm weather, keeps your legs covered in the cold, and has reflective accents to keep you safe. The Ray Jean is sure to make you feel great while making your cycling friends jealous.</p>",
              "published_at": "2018-06-30T03:28:24-04:00",
              "created_at": "2018-06-30T03:21:36-04:00",
              "vendor": "Club Ride Appparel",
              "type": "Apparel",
              "tags": [
                "Accessories",
                "Apparel",
                "Pants"
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
                  "id": 12543438323795,
                  "title": "31",
                  "option1": "31",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 31",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 31",
                  "public_title": "31",
                  "options": [
                    "31"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438356563,
                  "title": "32",
                  "option1": "32",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 32",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 32",
                  "public_title": "32",
                  "options": [
                    "32"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438389331,
                  "title": "33",
                  "option1": "33",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 33",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 33",
                  "public_title": "33",
                  "options": [
                    "33"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438422099,
                  "title": "34",
                  "option1": "34",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 34",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 34",
                  "public_title": "34",
                  "options": [
                    "34"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1530343296",
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1530343296",
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1530343296"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1530343296",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "31",
                    "32",
                    "33",
                    "34"
                  ]
                }
              ],
              "url": "/products/ray-jean?pr_prod_strat=collection_fallback&pr_rec_pid=1351125074003&pr_ref_pid=1351125106771&pr_seq=uniform",
              "media": [
                {
                  "alt": null,
                  "id": 1379424927827,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1569177889",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379424960595,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1569177889",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379424993363,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1569177889",
                  "width": 1200
                }
              ],
              "available_variants_count": 4,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296",
              "price_formatted": "$1,023.00",
              "compare_at_price_formatted": null
            },
            {
              "id": 1351129989203,
              "title": "650C 45mm Micro Wheelset",
              "handle": "650c-micro-wheelset",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p>Designed for speed and style in a more compact package, these Pure Fix double-walled aluminum wheelsets are size 650C with a 45mm rim depth, front and rear. Our wheels include name-brand and laser-etched, 120 mm KT Quando hubs. Our rear wheels include flip-flop hubs with a pre-attached 16T fixed cog along with a 16T freewheel cog for single-speed riding. Front and rear wheels feature 32 spokes each and all wheelsets include nylon rim-strips to protect against sharp edges and prevent tube puncture.</p>\n<p>We recommend using any style of 650C tire (tires and tubes not included).<br> <br> List of Specs:</p>\n<ul>\n<li>650C</li>\n<li>45mm rim depth</li>\n<li>Double-walled aluminum</li>\n<li>120mm KT Quando hubs</li>\n<li>Non-sealed</li>\n<li>Flip-flop rear hub</li>\n<li>Comes with pre-attached 16T fixed and freewheel cog</li>\n<li>32 spokes per wheel</li>\n<li>Includes nylon rim strips</li>\n<li>3.5 lbs per wheel</li>\n<li>\n<span style=\"font-size: 14px; line-height: 1.5;\">Perfect for our </span><a href=\"http://purefixcycles.com/collections/micro-series\" style=\"font-size: 14px; line-height: 1.5;\">Micro Line</a>\n</li>\n</ul>",
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
              "url": "/products/650c-micro-wheelset?pr_prod_strat=collection_fallback&pr_rec_pid=1351129989203&pr_ref_pid=1351127826515&pr_seq=uniform",
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
            },
            {
              "id": 1351127924819,
              "title": "Zulu",
              "handle": "the-zulu-glow-fixie",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\" rel=\"noopener noreferrer\">Pure Fix Cycles</a></em></p>\n<p>Get ready to take your night riding to a whole new level. After months of experimentation, we've perfected the GLOW, our newest line. The name says it all, it actually glows. The paint is solar-activated, so just give your bike an hour of daytime sun for an hour plus of night-time fun. Whether you're a night owl, a raver, or just want to trip out your friends, this is the bike for you.</p>",
              "published_at": "2018-06-30T03:25:29-04:00",
              "created_at": "2018-06-30T03:25:32-04:00",
              "vendor": "Pure Fix Cycles",
              "type": "Glow Series",
              "tags": [
                "47cm",
                "50cm",
                "54cm",
                "58cm",
                "Bicycles",
                "Bike",
                "College Fixie",
                "Fixed Gear",
                "Fixie",
                "Glow",
                "Glow Bikes",
                "Glow In The Dark",
                "Glow Series",
                "Pure Fix Cycles",
                "Urban Fixie",
                "White"
              ],
              "price": "$3,139.00",
              "price_min": 313900,
              "price_max": 471300,
              "available": true,
              "price_varies": true,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543450251347,
                  "title": "50 cm",
                  "option1": "50 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Small",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 50 cm",
                  "public_title": "50 cm",
                  "options": [
                    "50 cm"
                  ],
                  "price": 313900,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639737",
                  "price_formatted": "$3,139.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                },
                {
                  "id": 12543450284115,
                  "title": "54 cm",
                  "option1": "54 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Medium",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 54 cm",
                  "public_title": "54 cm",
                  "options": [
                    "54 cm"
                  ],
                  "price": 392600,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639744",
                  "price_formatted": "$3,926.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                },
                {
                  "id": 12543450316883,
                  "title": "58 cm",
                  "option1": "58 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Large",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 58 cm",
                  "public_title": "58 cm",
                  "options": [
                    "58 cm"
                  ],
                  "price": 471300,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639751",
                  "price_formatted": "$4,713.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1530343533"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1530343533",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "50 cm",
                    "54 cm",
                    "58 cm"
                  ]
                }
              ],
              "url": "/products/the-zulu-glow-fixie?pr_prod_strat=collection_fallback&pr_rec_pid=1351127924819&pr_ref_pid=1351127826515&pr_seq=uniform",
              "media": [
                {
                  "alt": null,
                  "id": 1379436036179,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436068947,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436101715,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1569177892",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379436134483,
                  "position": 4,
                  "preview_image": {
                    "aspect_ratio": 1.501,
                    "height": 933,
                    "width": 1400,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.501,
                  "height": 933,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1569177892",
                  "width": 1400
                },
                {
                  "alt": null,
                  "id": 1379436167251,
                  "position": 5,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436200019,
                  "position": 6,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436232787,
                  "position": 7,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436265555,
                  "position": 8,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436298323,
                  "position": 9,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1569177892",
                  "width": 2048
                }
              ],
              "available_variants_count": 3,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533",
              "price_formatted": "$3,139.00",
              "compare_at_price_formatted": null
            }
          ]
        }
        ```

3. Upsells

    ```jsx
    sellify.ucd.filters.upsells.push(function(products){
    	console.log({upsells: products});
    });
    ```

    - Toggle sample variables

        ```json
        {
          "upsells": [
            {
              "id": 1351125074003,
              "title": "Club Ride Ray Jean",
              "handle": "ray-jean",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p class=\"p1\">\"You rode here in jeans?!\" Your envious friends gasp, \"Aren't they heavy?\" Not these. The Ray Jean was designed specifically for riders who like the comfort of bike-wear without all the spandex and sideways glances it causes once you're away from your ride. The Ray Jean is made with StretchRide2 (the better-than-the-original sequel to StretchRide) and is 30% lighter than standard denim. It breathes well in warm weather, keeps your legs covered in the cold, and has reflective accents to keep you safe. The Ray Jean is sure to make you feel great while making your cycling friends jealous.</p>",
              "published_at": "2018-06-30T03:28:24-04:00",
              "created_at": "2018-06-30T03:21:36-04:00",
              "vendor": "Club Ride Appparel",
              "type": "Apparel",
              "tags": [
                "Accessories",
                "Apparel",
                "Pants"
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
                  "id": 12543438323795,
                  "title": "31",
                  "option1": "31",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 31",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 31",
                  "public_title": "31",
                  "options": [
                    "31"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438356563,
                  "title": "32",
                  "option1": "32",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 32",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 32",
                  "public_title": "32",
                  "options": [
                    "32"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438389331,
                  "title": "33",
                  "option1": "33",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 33",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 33",
                  "public_title": "33",
                  "options": [
                    "33"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                },
                {
                  "id": 12543438422099,
                  "title": "34",
                  "option1": "34",
                  "option2": null,
                  "option3": null,
                  "sku": "Clubride - Jayjean - 34",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Club Ride Ray Jean - 34",
                  "public_title": "34",
                  "options": [
                    "34"
                  ],
                  "price": 102300,
                  "weight": 227,
                  "compare_at_price": null,
                  "inventory_management": null,
                  "barcode": null,
                  "price_formatted": "$1,023.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1530343296",
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1530343296",
                "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1530343296"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1530343296",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "31",
                    "32",
                    "33",
                    "34"
                  ]
                }
              ],
              "url": "/products/ray-jean?pr_prod_strat=collection_fallback&pr_rec_pid=1351125074003&pr_ref_pid=1351125106771&pr_seq=uniform",
              "media": [
                {
                  "alt": null,
                  "id": 1379424927827,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean1.jpg?v=1569177889",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379424960595,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean3.jpg?v=1569177889",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379424993363,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1569177889"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/jayjean2.jpg?v=1569177889",
                  "width": 1200
                }
              ],
              "available_variants_count": 4,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/jayjean1_large.jpg?v=1530343296",
              "price_formatted": "$1,023.00",
              "compare_at_price_formatted": null
            },
            {
              "id": 1351129989203,
              "title": "650C 45mm Micro Wheelset",
              "handle": "650c-micro-wheelset",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\">Pure Fix Cycles</a></em></p><p>Designed for speed and style in a more compact package, these Pure Fix double-walled aluminum wheelsets are size 650C with a 45mm rim depth, front and rear. Our wheels include name-brand and laser-etched, 120 mm KT Quando hubs. Our rear wheels include flip-flop hubs with a pre-attached 16T fixed cog along with a 16T freewheel cog for single-speed riding. Front and rear wheels feature 32 spokes each and all wheelsets include nylon rim-strips to protect against sharp edges and prevent tube puncture.</p>\n<p>We recommend using any style of 650C tire (tires and tubes not included).<br> <br> List of Specs:</p>\n<ul>\n<li>650C</li>\n<li>45mm rim depth</li>\n<li>Double-walled aluminum</li>\n<li>120mm KT Quando hubs</li>\n<li>Non-sealed</li>\n<li>Flip-flop rear hub</li>\n<li>Comes with pre-attached 16T fixed and freewheel cog</li>\n<li>32 spokes per wheel</li>\n<li>Includes nylon rim strips</li>\n<li>3.5 lbs per wheel</li>\n<li>\n<span style=\"font-size: 14px; line-height: 1.5;\">Perfect for our </span><a href=\"http://purefixcycles.com/collections/micro-series\" style=\"font-size: 14px; line-height: 1.5;\">Micro Line</a>\n</li>\n</ul>",
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
              "url": "/products/650c-micro-wheelset?pr_prod_strat=collection_fallback&pr_rec_pid=1351129989203&pr_ref_pid=1351127826515&pr_seq=uniform",
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
            },
            {
              "id": 1351127924819,
              "title": "Zulu",
              "handle": "the-zulu-glow-fixie",
              "description": "<p><em>This is a demonstration store. You can purchase products like this from <a href=\"https://www.purefixcycles.com\" target=\"_blank\" rel=\"noopener noreferrer\">Pure Fix Cycles</a></em></p>\n<p>Get ready to take your night riding to a whole new level. After months of experimentation, we've perfected the GLOW, our newest line. The name says it all, it actually glows. The paint is solar-activated, so just give your bike an hour of daytime sun for an hour plus of night-time fun. Whether you're a night owl, a raver, or just want to trip out your friends, this is the bike for you.</p>",
              "published_at": "2018-06-30T03:25:29-04:00",
              "created_at": "2018-06-30T03:25:32-04:00",
              "vendor": "Pure Fix Cycles",
              "type": "Glow Series",
              "tags": [
                "47cm",
                "50cm",
                "54cm",
                "58cm",
                "Bicycles",
                "Bike",
                "College Fixie",
                "Fixed Gear",
                "Fixie",
                "Glow",
                "Glow Bikes",
                "Glow In The Dark",
                "Glow Series",
                "Pure Fix Cycles",
                "Urban Fixie",
                "White"
              ],
              "price": "$3,139.00",
              "price_min": 313900,
              "price_max": 471300,
              "available": true,
              "price_varies": true,
              "compare_at_price": null,
              "compare_at_price_min": 0,
              "compare_at_price_max": 0,
              "compare_at_price_varies": false,
              "variants": [
                {
                  "id": 12543450251347,
                  "title": "50 cm",
                  "option1": "50 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Small",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 50 cm",
                  "public_title": "50 cm",
                  "options": [
                    "50 cm"
                  ],
                  "price": 313900,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639737",
                  "price_formatted": "$3,139.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                },
                {
                  "id": 12543450284115,
                  "title": "54 cm",
                  "option1": "54 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Medium",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 54 cm",
                  "public_title": "54 cm",
                  "options": [
                    "54 cm"
                  ],
                  "price": 392600,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639744",
                  "price_formatted": "$3,926.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                },
                {
                  "id": 12543450316883,
                  "title": "58 cm",
                  "option1": "58 cm",
                  "option2": null,
                  "option3": null,
                  "sku": "The Zulu - Large",
                  "requires_shipping": true,
                  "taxable": true,
                  "featured_image": null,
                  "available": true,
                  "name": "Zulu - 58 cm",
                  "public_title": "58 cm",
                  "options": [
                    "58 cm"
                  ],
                  "price": 471300,
                  "weight": 28123,
                  "compare_at_price": null,
                  "inventory_management": "shopify",
                  "barcode": "741360639751",
                  "price_formatted": "$4,713.00",
                  "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533"
                }
              ],
              "images": [
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1530343533",
                "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1530343533"
              ],
              "featured_image": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1530343533",
              "options": [
                {
                  "name": "Size",
                  "position": 1,
                  "values": [
                    "50 cm",
                    "54 cm",
                    "58 cm"
                  ]
                }
              ],
              "url": "/products/the-zulu-glow-fixie?pr_prod_strat=collection_fallback&pr_rec_pid=1351127924819&pr_ref_pid=1351127826515&pr_seq=uniform",
              "media": [
                {
                  "alt": null,
                  "id": 1379436036179,
                  "position": 1,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436068947,
                  "position": 2,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0004_Glow_Zulu_4.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436101715,
                  "position": 3,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 800,
                    "width": 1200,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 800,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/zulu_1201.jpg?v=1569177892",
                  "width": 1200
                },
                {
                  "alt": null,
                  "id": 1379436134483,
                  "position": 4,
                  "preview_image": {
                    "aspect_ratio": 1.501,
                    "height": 933,
                    "width": 1400,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.501,
                  "height": 933,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/amazonzulu.jpg?v=1569177892",
                  "width": 1400
                },
                {
                  "alt": null,
                  "id": 1379436167251,
                  "position": 5,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0005_Glow_Zulu_3.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436200019,
                  "position": 6,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0003_Glow_Zulu_5.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436232787,
                  "position": 7,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0001_Glow_Zulu_7.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436265555,
                  "position": 8,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0002_Glow_Zulu_6.jpg?v=1569177892",
                  "width": 2048
                },
                {
                  "alt": null,
                  "id": 1379436298323,
                  "position": 9,
                  "preview_image": {
                    "aspect_ratio": 1.5,
                    "height": 1365,
                    "width": 2048,
                    "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1569177892"
                  },
                  "aspect_ratio": 1.5,
                  "height": 1365,
                  "media_type": "image",
                  "src": "https://cdn.shopify.com/s/files/1/2325/8929/products/ZULU_WEB_0000_Glow_Zulu_8.jpg?v=1569177892",
                  "width": 2048
                }
              ],
              "available_variants_count": 3,
              "img": "//cdn.shopify.com/s/files/1/2325/8929/products/ZULU_2014_SEAMLESS_SIDE_KENDA_WEB_large.jpg?v=1530343533",
              "price_formatted": "$3,139.00",
              "compare_at_price_formatted": null
            }
          ]
        }
        ```

4. Tiered Free Items

    ```jsx
    sellify.ucd.filters.tiered_free_items.push(function(products){
    	console.log({tiered_free_items: products});
    });
    ```

    - Toggle sample variables

        ```json
        {
        	"tiered_free_items" : 
        	[
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
        	    "price": "$708.00",
        	    "price_min": 70800,
        	    "price_max": 70800,
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
        	        "price": 70800,
        	        "weight": 227,
        	        "compare_at_price": null,
        	        "inventory_management": null,
        	        "barcode": null,
        	        "price_formatted": "$708.00",
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
        	        "price": 70800,
        	        "weight": 227,
        	        "compare_at_price": null,
        	        "inventory_management": null,
        	        "barcode": null,
        	        "price_formatted": "$708.00",
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
        	        "price": 70800,
        	        "weight": 227,
        	        "compare_at_price": null,
        	        "inventory_management": null,
        	        "barcode": null,
        	        "price_formatted": "$708.00",
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
        	        "price": 70800,
        	        "weight": 227,
        	        "compare_at_price": null,
        	        "inventory_management": null,
        	        "barcode": null,
        	        "price_formatted": "$708.00",
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
        	    "price_formatted": "$708.00",
        	    "compare_at_price_formatted": null,
        	    "unlocked": true,
        	    "locked": false,
        	    "unlock_price": "$300.00",
        	    "progress": 863,
        	    "remaining": -2289
        	  }
        	]
        }
        ```

5. Special Offer Notifications

    ```jsx
    sellify.ucd.filters.cart_final.push(function(cart){
    	console.log({special_offers: cart.special_offers});
    });
    ```

    - Toggle sample variables

        ```json
        {
        	 "special_offers": {
            "tiers": [
              {
                "message": "CONGRATULATIONS, YOU'VE QUALIFIED FOR FREE SHIPPING.",
                "value": 300,
                "progress": 100,
                "remaining_amount": 0,
                "remaining": 0,
                "qualified": true
              }
            ],
            "progress": 100,
            "show_progress_bar": true,
            "progress_tier": {
              "message": "CONGRATULATIONS, YOU'VE QUALIFIED FOR FREE SHIPPING.",
              "value": 300,
              "progress": 100,
              "remaining_amount": 0,
              "remaining": 0,
              "qualified": true
            }
          }
        }
        ```