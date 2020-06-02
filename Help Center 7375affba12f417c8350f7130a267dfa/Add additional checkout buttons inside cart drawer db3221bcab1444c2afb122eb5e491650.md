# Add additional checkout buttons inside cart drawer

This is an advanced tutorial and proceed only if understand the risks.

[https://www.loom.com/share/2af94a729595425299d66c080aad7973](https://www.loom.com/share/2af94a729595425299d66c080aad7973)

1. Create a new snippet in your theme and set name `additional-checkout-buttons.liquid` and add following code:

    ```html
    <script type="text/template" id="additional-checkout-buttons">
    {% if additional_checkout_buttons %}
      <div class="additional-checkout-buttons">
        {{ content_for_additional_checkout_buttons }}
      </div>
    {% endif %}
    </script>

    <script type="text/javascript">
    window.addEventListener('Sellify::UCD::CartBuilt', function(e){
      if(document.getElementById('ucd-additional-checkout-buttons') && document.getElementById('additional-checkout-buttons'))
      {
        document.getElementById('ucd-additional-checkout-buttons').innerHTML = document.getElementById('additional-checkout-buttons').innerHTML;

        if(window.Shopify && Shopify.StorefrontExpressButtons)
        {
          Shopify.StorefrontExpressButtons.initialize();
        }
      }
    });
    </script>

    <style type="text/css">
    #ucd-additional-checkout-buttons {padding:0 20px 20px;}
    #ucd-additional-checkout-buttons .additional-checkout-button {display:block;width:100% !important;}
    #ucd-additional-checkout-buttons .additional-checkout-button + .additional-checkout-button{
        margin-top: 10px !important;
    }
    </style>
    ```

2. Open `theme.liquid` file and add following code before ending `</body>` tag and save the file:

    ```html
    {% include 'additional-checkout-buttons' %}
    ```

3. Open [ULTIMATE Cart Drawer](https://ucd.sellifyapps.com) app and visit [Themes](https://ucd.sellifyapps.com/themes) page. 
4. `Edit code` for Live Theme and Edit `Cart Template`. 
5. Add following code before the submit button and hit Save

    ```html
    <div id="ucd-additional-checkout-buttons"></div>
    ```