Additional resources that can be useful:

1. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#view_item
2. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_to_cart
3. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#begin_checkout
4. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_shipping_info
5. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#add_payment_info
6. https://developers.google.com/analytics/devguides/collection/ga4/reference/events?sjid=11470055494011769802-EU&client_type=gtag#purchase

Please note that these links include a gtag call, and not a dataLayer push. _We want a dataLayer push_ which is why I've included that in each snippets.

The correct orders of the events are:

1."view_item"

2."add_to_cart"

3."begin_checkout"

4."add_shipping_info"

5."add_payment_info"

6."purchase"


1. These are the instructions about the "_view_item_" event:
- "push" the code once the user lands on a product page like **XXXXXX TO BE ADDED**
- a user can view more products during one single session, therefore more view_item events can be pushed during a throughout it.

  

3. These are the instructions about the "_add_to_cart_" event:
- "push" the code once the user clicks the **XXXXXX TO BE ADDED**
- if a user then initiates the checkout, then goes back to and add another product, push again this event. 


3. These are the instructions about the "_begin_checkout_" event:
- "push" the code once the user, when seeing the cart, clicks the **XXXXXX TO BE ADDED**
- If a user then goes back to the cart page, do _not_ "push" it again (to prevent double tracking).


4. These are the instructions about the "_add_shipping_info_" event:
- "push" the code once the user, when checking out, after inserting its billing info, clicks the **XXXXXX TO BE ADDED**
- If a user then goes back to the cart page, do not "push" it again (to prevent double tracking).


5. These are the instructions about the "_add_payment_info_" event:
- "push" the code once the user, when checking out, after inserting its payment details, clicks the **XXXXXX TO BE ADDED**
- Do not "push" the code when a user reaches the thank you page.
- If a user then goes back to the cart page, do not "push" it again (to prevent double tracking).


6. These are the instructions about the "_purchase_" event:
- "push" the code once the user has reached the final TY page (in the case if there are upsells for example).
- If a user then refreshes the page, or visit it later (via email for example), do not "push" it again (to prevent double tracking).
- The data layer script is placed just above the GTM snippet in the head of the document.


If you have any doubts please message me on Slack or email me. 
