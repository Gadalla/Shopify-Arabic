# Shopify Arabic Translation
## Into
This repo contains Arabic translation for Shopify store. Only the front end (visitor website) will be translated along with notification emails. You will need to buy a shopify theme that switch to RTL when Arabic language is selected.

## Installation instructions
### Store Front End Translation
- Add the ar.json file to Locales folder in your theme
- If you have the ar.json already exist in your theme, replace the theme file or copy the cotent in the ar.json file in your theme ar.json,

### Email Notification Translation
#### Arabic Only Store (One Language Store)
- Go to your store back end YourStore.myshopify.com/admin
- Then to Settings >> Notifications
- Copy the content of each file in the Email Notifications folder and paste it in the notification (Email tab)  with the same name respectively. The name of the files and folders are intuitive

#### Multi Language Store
- Go to your store back end YourStore.myshopify.com/admin
- Then to Settings >> Notifications
- Copy the content of each file in the Email Notifications folder and paste it in the ar section in the code below. Copy and paste the notification of the other languge(s) in there place in the code. Shopify will send the notification email in the language of the website's visitor is using. Use a text editor for this step. In the exmaple below, there are three languages, Arabic, French, and English.
- Copy the code created and paste it in the notification (Email tab) with the same name respectively. The name of the files and folders are intuitive

```liquid
{% case customer_locale %}   
{% when 'ar' %}
الايميل بالعربي هنا (لصق من الملف)
{% when 'fr' %}
EMAIL EN FRANÇAIS ICI
{% else %}  
EMAIL IN THE ORIGINAL LANGUAGE (English) HERE
{% endcase %}
```

- You can use the same code above to translate Email notification title, for example:

```
{% case customer_locale %}
{% when 'ar' %}
{{shop.name}} - تم تأكيد الطلب {{name}}
{% when 'fr' %}
{{shop.name}} - Achat {{name}} confirmé
{% else %}
{{shop.name}} - Order {{name}} confirmed
{% endcase %}
```

## Theme Support
The below themes support switching the website's layout to RTL on language select. The first theme is used when creating this repo. The theme developer customized it to support RTL on language select.
- Woodstock [Themeforest link](https://themeforest.net/item/woodstock-electronics-shopify-sections-theme/24338624)