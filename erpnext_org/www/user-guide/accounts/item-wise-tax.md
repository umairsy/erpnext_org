### Managing Itemwise Tax in ERPNext

By dafault, taxes selected in the Tax and Other Charges in transactions are applied on all the items. You should follow these steps to have specific tax rates applied on items.

**Step 1: Mention taxes applicanle on item in the Item master**

Item master has tax table where you can list taxes which will be applied on it.

![Item wise Tax](assets/erpnext_org/images/erpnext/item-wise-tax.png)

Tax rate mentioned in the item master gets preference over tax rate entered in the transactions. 

For example, if you provide tax rate for VAT as 10% for item ABC, where for same VAT ledger 12% rate is entered in the Sales Order/Invoice, for item ABC, tax rate applied would be 10%, as mentioned in the item master.

**Step 2: Setup Taxes and Other Charges**

In Taxes and Other Charges master, you should select all the applicable taxes which could be applicable on item.

For example, if few items has VAT 5 applied on them, other has Service Tax applied, and some other has Excise Duty applicable, then you tax master should have all these taxes selected.

![item wise tax master](assets/erpnext_org/images/erpnext/item-wise-tax-master.png)

**Step 3: Set Tax Rate as Zero**

In the Taxes and Other Charges master, tax rate will be updated as ZERO. It means, tax rate applicable on items will be pulled from the respective Item master. While for other items, 0% tax will be applied, means no other taxes will be applied on that item.

Based on the above setting, you will have taxes applied on items as mentioned in the respective item master. Check following for an instance.

![item wise tax calculation](assets/erpnext_org/images/erpnext/item-wise-tax-calc.png)