Selling Setting is where you can define propertiese which will be applied in your selling transactions. Let's check into each property one by one.

####1. Customer Naming By

When customer is saved, system generated unique ID for that Customer. Using that Customer ID, you can select Customer in other transactions.

Bydefault Customer will be saved with Customer Name. If you wish to save Customer using a naming series, you should set Customer Naming By as "Naming Series".

![Customer Naming By](assets/erpnext_org/images/erpnext/ss-customer-naming-by.png)

Example of Customer Id's saved in Naming Series - `CUST00001,CUST00002, CUST00003...` and so on.

You can set Naming Series for customer naming from:

`Setup > Settings > Naming Series`

Click [here](https://erpnext.com/user-guide/setting-up/document-naming-series) to learn about how to use Naming Series tool.

####2. Campaign Naming By

Just like for Customer, you can also configure as how ID will be generated for the Campaign master. Bydefault Campaign will be saved with Campaign Name provided while its creation.

![Campaign Naming By](assets/erpnext_org/images/erpnext/ss-campaign-naming-by.png)

####3. Default Customer Group

Customer Group in this field will be auto-updated when you open new Customer form.

![Default Customer Group](assets/erpnext_org/images/erpnext/ss-default-customer-group.png)

While converting Quotation created for Lead into Sales Order, system attempts to convert Lead into Customer in the backend. While creating Customer in the backend, system pickup Customer Group and Territory as defined in the Selling Setting. If system doesn't find any values, then following validation message will be raised.

![Default Customer Group Error](assets/erpnext_org/images/erpnext/ss-customer-group-error.png)

To resolve this, you should:

Either manually convert Lead into Customer, and define Customer Group and Territory manually while creating Customer.

Or 

Define Default Customer Group and Territory in the Selling Setting. Then you should have Lead automatically converted into Customer when convert Quotation into Sales Order.

####4. Default Territory

Territory defined in this field will be auto-updated in the Territory field of Customer master.

![Default Territory](assets/erpnext_org/images/erpnext/ss-default-territory.png)

Just like Customer Group, Territory is also checked when system tries creating Customer in the backend.

####5. Default Price List

Price List set in this field will be auto-updated in the Price List field of Sales transactions.

![Default Price List](assets/erpnext_org/images/erpnext/ss-default-price-list.png)

####6. Sales Order Required

If you wish to make Sales Order creation mandatory before creation of Sales Invoice, then you should set Sales Order Required field as Yes. Bydefault, this will be "No" for a value.

![Sales Order Required](assets/erpnext_org/images/erpnext/ss-sales-order-required.png)

####7. Delivery Note Required

To make Delivery Note creation as mandatory before Sales Invoice creation, you should set this field as "Yes". It will be "No" by default.

![Delivery Note Required](assets/erpnext_org/images/erpnext/ss-delivery-note-required.png)

####8. Maintain Same Rate Throughout Sales Cycle

System bydefault validates that item price will be same throughout sales cycle (Sales Order - Delivery Note - Sales Invoice). If you could have item price changing within the cycle, and you need to bypass validation of same rate throughout cycle, then you should uncheck this field and save.

![Same Rate Throughout](assets/erpnext_org/images/erpnext/ss-same-rate-throughout.png)

####9. Allow User to Edit Price List Rate in Transaction

Item table of the sale transactions has field called Price List Rate. This field be non-editale by default in all the sales transactions. This is to ensure that price of an item is fetched from Item Price record, and user is not able to edit it.

If you need to enable user to edit Item Price, fetched from Price List of an item, you should uncheck this field.

![Edit Price List Rate](assets/erpnext_org/images/erpnext/ss-edit-price-list-rate.png)