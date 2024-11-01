=== Wrapper Checkout for WooCommerce and Cardpointe ===
Contributors: Use Wrapper
Tags: woocommerce, payments, ecommerce, shops
Requires at least: 4.0
Tested up to: 6.3
Stable tag: 1.3.5
Requires PHP: 5.4
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html


== Description ==
"Wrapper" is a WooCommerce extension to redirect customer's to external payment gateway hosted payment pages. Wrapper is a powerful, secure, and seamless solution for e-commerce vendors and store owners who are already using <a href="https://wordpress.org/plugins/woocommerce/">WooCommerce</a> for its stunning product display and functionality. This plugin offers an additional layer to WooCommerce by integrating the <a href="https://cardconnect.com/signup">CardPointe Gateway</a> as a new payment option, providing an enhanced and efficient checkout experience for your customers.

== Requirements ==
- **Payment Gateway** This plugin currently supports the CardPointe Gateway. Reach out through support forums to request an additional gateway. 
- **Hosted Payment Page** This plugin will redirect customers to an external payment page and therefore an active HPP is necessary.
- **WooCommerce Extensions** may break the functionality of this plugin, please triage and submit bug reports to our support forums. 

== Frequently Asked Questions ==

= What changes to make inside the Design tab? =

* Add a hidden custom field called woo_id 
* Drag and drop the "Line Items" element into the page

= What changes to make inside the Connect tab? =

* Create an invoice with the Order Line Items (Column 1 = Name, Column 2 = Quantity, Column 3 = Price), then create a line item (Orange, 5, 5) and click "build link". This saves the line-item configuration for future links. 
* Add your website URL to the redirect field. You can even create a page on WordPress that states "Payment Complete, please check your email for confirmation", etc. 
* WordPress by default doesn't know when a payment occurs on the HPP. To support this option, please add the following URL to the webhook URL __https://tranquil-oasis-93890.herokuapp.com/callback__

= What changes to make inside the Setup tab? =

* Change from V3 to V2 Captcha

== explanation of the plugin settings == 

* __Enable/Disable__ - Enables plugin on the WooCommerce Checkout Page
* __Description__ - This value is displayed to customers at your WooCommerce checkout area.
* __Tax Name__ - Default is "tax", change the value to add your own name for the tax line item.
* __Shipping Name__ - Default is "shipping", change the value to add your own name for the tax line item.
* __ACH?__ Check this box if your processor supports ACH transactions.
* __Testmode__ - Enable this to link your customers to the URL set below (test_hpp_url)
* __test_hpp_url__ - The URL of your testing hosted payment page, please include the beginning part ONLYINCLUDETHISPART. https://<ONLYINCLUDETHISPART>.securepayments.cardpointe.com
* __prod_hpp_url__ - The URL of your hosted payment page, please include the part highlighted in bold. https://__cpswoo__.securepayments.cardpointe.com

### Dev/Test Admin Settings
* __test_hpp_url__ - The URL of your hosted payment page, please include the part highlighted in bold. https://__testcpswoo__.securepayments.cardpointe.com
* __api_key__ - This value isn't currently supported and is not required.


== Changelog ==
1.3.5
Tested up to 6.3 WordPress
Tested up to 8.0 WooCommerce
Additional Input Validation and URL encoding for security
1.3.4
Ability to update tax and shipping descriptors
1.3.3 
Config option *redirectThruAPI* is disabled by default. URL redirection is created on the website.
1.3.2
Updates to calculating the price by substituting product class for order class.
1.3.1
Fixes: https://i.imgur.com/omR49qs.png
>Shipping and Taxes are no longer calculated in the total price, or line items.
Support for WooCommerce automatic notification of successful payment
Troubleshooting and usage metric's added through in house connections

== Upgrade Notice ==
No support provided