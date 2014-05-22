# Buying

<p class="lead"> Buying raw materials when there is no Stock can be done by raising Material Requests and completing the purchase cycle. The purchase cycle includes making Purchase Orders and Purchase Receipts along with Purchase Invoice and Payment Entry through Journal Voucher.</p>

### Purchase Order

Purchase Order (PO) is a commercial document and first official offer issued by a buyer to a seller, indicating types, quantities, and agreed prices for the products [1]

You can make a Purchase Order from a Material Request or by directly going to:

> Buying > Purchase Order > New Purchase Order 


__Figure 1: Make Purchase Order__

![Purchase Order](/assets/erpnext_org/images/erpnext/e-t-o-purchase-order-childbed.png)

Make the Purchase Order, save and submit it. After saving, click on 'Make Purchase Receipt'. Save and submit the Purchase Receipts. 

### Purchase Receipt

Purchase Receipt is a record that is made when a material is received. It is also known as a Goods Received Note (GRN). It contains detail information of the Items purchased including the name of the Item, the price as well as the time when the purchase has been made.

You can make a Purchase Receipt from the Purchase Order or directly from the Stock module.

> Stock > Purchase Receipt > New Purchase Receipt

__Figure 3: Make Purchase Receipt__

![Purchase Receipt](/assets/erpnext_org/images/erpnext/e-t-o-purchase-receipt-childbed.png)

> Note that only when the Purchase Receipt is submitted, the Stock balance is updated. To see the Stock balance go to the Stock module and select the Stock Balance Report from the Reports section.

When the Purchase Receipt is saved and submitted, click on the Action button and make Purchase Invoice.

### Purchase Invoice

A Purchase Invoice can be used to prove that something was bought and an amount was paid for it.

> Accounts > Purchase Invoice > New Purchase Invoice

__Figure 4: Purchase Invoice__

![Purchase Invoice](/assets/erpnext_org/images/erpnext/e-t-o-purchase-invoice.png)

Save and submit the Purchase Invoice. Click on the Action button and make Payment Entry.

### Payment Entry

Payment Entry is done to book all accounting transactions in your system. It is an important step of Book Keeping.

> Accounts > Journal Voucher > New Journal Voucher

__Figure 5: Payment Entry__

![Payment Entry](/assets/erpnext_org/images/erpnext/e-t-o-payment-entry-childbed.png)

Save and submit the Payment Entry. This was a complete cycle for the Material Request of Nut Bolts. Now repeat the same process for other requests which were generated by the Production Planning Tool.

Material Request > Purchase Order > Purchase Receipt > Purchase Invoice > Journal Voucher. 

![Material Request Flowchart](/assets/erpnext_org/images/erpnext/material-request-flowchart-image.png)

In a similar fashion, go to each and every Material Request created for this order and complete the cycle. Once Buying is done you can proceed to manufacture.


Next : [Manufacturing](/apps/erpnext/guide-books/engineer-to-order/stock-entry)


---

References

1. [Wikipedia: Purchase Order](http://en.wikipedia.org/wiki/Purchase_order)