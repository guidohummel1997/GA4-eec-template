Additional resources that can be useful:

https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#view_item
https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_to_cart
https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#begin_checkout
https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_shipping_info
https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_payment_info
https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#purchase

Please note that these links include a gtag call, and not a dataLayer push. _We want a dataLayer push_ which is why I've included that in each snippets.

The correct orders of the events are:

1."view_item"
2."add_to_cart"
3."begin_checkout"
4."add_shipping_info"
5."add_payment_info"
6."purchase"

3. These are the detailed instructions about the "_begin_checkout_" event:
"push" the code once the user, when seeing the cart, clicks the **XXXXXX TO BE ADDED**
If a user then goes back to the cart page, do not "push" it again (to prevent double tracking).

4. These are the detailed instructions about the "_add_shipping_info_" event:
"push" the code once the user, when checking out, after inserting its billing info, clicks the **XXXXXX TO BE ADDED**
If a user then goes back to the cart page, do not "push" it again (to prevent double tracking).

5. These are the detailed instructions about the "_add_payment_info_" event:
"push" the code once the user, when checking out, after inserting its payment details, clicks the **XXXXXX TO BE ADDED**
Do not "push" the code when a user reaches the thank you page.
If a user then goes back to the cart page, do not "push" it again (to prevent double tracking).

6. These are the detailed instructions about the "_purchase_" event:
"push" the code once the user has reached the TY page.
If a user then refreshes the page, or visit it later (via email for example), do not "push" it again (to prevent double tracking).


If you have any doubts please message me on Slack.
