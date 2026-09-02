# User ID Tag Template for GTM

Use this GTM web tag template to set a first-party user ID cookie (`__ln_uid`). The value is a random UUID, stored for one year, generated once per browser. Use it as an external ID for Advanced Matching in Meta so browser and server events for the same visitor match, which improves Event Match Quality.

The cookie is only written when `analytics_storage` consent is granted. Without consent the tag waits and writes the cookie as soon as consent comes in, so it is safe to fire on every page.

## Installation

1. Download [`template.tpl`](template.tpl).
2. In GTM, go to **Templates**, then **Tag Templates**, then **New**.
3. Open the menu in the top right, click **Import**, and select `template.tpl`.
4. Click **Save**.
5. Create a new tag of type **User ID** and fire it on **Initialization - All Pages**.

## Reading the value

Create a **1st Party Cookie** variable named `__ln_uid`. Pass it as `external_id` to your Meta pixel and to the Meta CAPI tag in server-side GTM. It works for any other platform that accepts a stable first-party identifier, too.

## Settings

The template has no fields. Cookie name, one-year lifetime and `SameSite=Lax` are fixed in the code.

## Companion templates

- [Shopify Custom Pixel](https://github.com/lucnugteren/shopify_custom_pixel) for a GTM dataLayer in Shopify checkout.
- [Restore GCLID tag template](https://github.com/lucnugteren/gtm_web_tag_template_restore_gclid) for Safari-stripped click IDs.
- [Purchase Count tag template](https://github.com/lucnugteren/gtm_web_tag_template_purchase_count) for new vs. returning customers in Google Ads.

More at [lucnugteren.com/resources](https://lucnugteren.com/resources).
