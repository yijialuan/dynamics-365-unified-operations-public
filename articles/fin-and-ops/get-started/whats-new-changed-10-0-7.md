---
# required metadata

title: Preview features in Finance and Operations version 10.0.7 (December 2019)
description: This topic describes features that are either new or changed in Finance and Operations version 10.0.7. This version will be released in November.
author: tonyafehr
manager: AnnBe
ms.date: 09/16/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 

# optional metadata

# ms.search.form: 
# ROBOTS: 
audience: Developer, IT Pro
# ms.devlang: 
ms.reviewer: tfehr
ms.search.scope:  Operations
# ms.tgt_pltfrm: 
ms.custom: 
ms.assetid: 
ms.search.region: Global
# ms.search.industry: 
ms.author: tfehr
ms.search.validFrom:  
ms.dyn365.ops.version: Release 10.0.7

---
# Preview features in Finance and Operations version 10.0.7 (December 2019)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

This topic describes features that are either new or changed in Finance and Operations version 10.0.7. This version has a build number of xx.x.xxx. While the general availability date is in December, the new features are available for early release in November. For more information about version 10.0.7, see [Additional resources](whats-new-changed-10-0-7.md#additional-resources).

To learn about the new features and changes in the latest releases of Microsoft Dynamics 365 Retail, see [Preview features in Dynamics 365 Retail version 10.0.7](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/get-started/whats-new-10-0-7).

## Feature heading

The **Budget register entries for quantity only** feature enables the ability to post a budget register entry with quantity-only amounts. For example, you could post a budget entry of 32 quantity with a price of zero, resulting in an amount of zero. You may then use this quantity within the context of a financial reporting report to determine a price per quantity.
https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/budgeting/basic-budgeting-overview-configuration

The **Budget register entries defaulting of amount type** feature enables the defaulting of amount type to revenue or expense based on the main account of the budget line.
https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/budgeting/basic-budgeting-overview-configuration

The **Ledger settlement by user** feature allows processing ledger settlement by user ID.  When enabled, a user will only see records in Advanced ledger settlement that have no user ID (not marked for settlement) or have their user ID (records they marked for settlement). Only the records marked by that user will be processed when choosing Settle marked transactions. A new button, Unmark for selected users, was also added to unmark records marked for settlement but not processed.  This could be used after a user leaves an organization. 

## Account groups selection for Chinese voucher types

This feature allows you to select accounts groups when setting up voucher types for China. 

### Enable the feature
1. Enable the feature in the **Workspaces > Feature management**.
2. Feature introduces a new table where voucher type setup is stored. To copy existing Chinese voucher types setup to a new table, go to **System administration > Periodic tasks > Database > Consistency check**. Expand **Program > General ledger** and mark **Restriction type for voucher** check box. 
3. Select **Check** in the **Check/Fix** field to check whether there are settings in existing setup to copy to a new table.
4. Select **Fix** in the **Check/Fix** field to copy settings from existing table to a new table.

### Set up Voucher type
1. Go to **General ledger > Journal setup > Chinese voucher type > Voucher type**.
2. Under the **Rules** FastTab, select the line with specific restriction.
2. Under the **Impacted accounts** FastTab, click **Add** and set up the accounts for the selected rule:
- In the **Account type** field, select **Ledger**, **Customer**, **Vendor**, **Project**, **Fixed assets**, **Bank**
- In the **Account code**, select **Account**, **Group**, or **All**. Note that the value **Group** is not available for **Ledger** account code.
- In the **Group number** field, select customer group, vendor group, project group, fixed asset group, or bank group respectively to the value in **Account type**, if you selected **Group** in the field **Account code**.
- In the **Account number** field, select ledger account, customer account, vendor account, project ID, fixed asset number, or bank account respectively value in **Account type**, if you selected **Table** in the field **Account code**

Find more details about how to set up Chinese voucher types in the topic [Set up Chinese vouchers](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/localizations/tasks/set-up-chinese-vouchers)

## Sort by resource in the project invoice proposal

The **Enable sorting by resource during project invoice proposal creation** feature enables the ability for the project accountant to sort the project transactions available for billing to be sorted by the resource when creating a new project invoice proposal. The grid displaying the available project transactions will have a separate field for Resource ID and Resource, allowing the user to filter and sort on the resource name. This feature is disabled by default and can be enabled in **Workspaces > Feature management**.
