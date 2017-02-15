---
# required metadata

title: Total cost allocation method
description: This article provides guidelines for using total cost allocation (TCA). TCA is a method of calculating the cost between the main formula item for a batch order and the co-products that are defined for the formula.
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-29 14 - 07 - 27
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 

# optional metadata

ms.search.form: BOMConsistOf, PmfFormulaCoBy
# ROBOTS: 
audience: Application User
# ms.devlang: 
# ms.reviewer: 2094
ms.search.scope: AX 7.0.0, Operations
# ms.tgt_pltfrm: 
ms.custom: 83852
ms.assetid: f1bd1918-290d-40ce-b3ad-717143261222
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0

---

# Total cost allocation method

This article provides guidelines for using total cost allocation (TCA). TCA is a method of calculating the cost between the main formula item for a batch order and the co-products that are defined for the formula.

Total cost allocation (TCA) is a method of calculating the cost between the main formula item for a batch order and the co-products that are defined for the formula. This method is dynamic. It calculates the cost as a weighted average between the quantities that are reported as finished for the formula item and the co-products. When TCA is used, you don't have to review cost allocations for every batch order. If TCA isn't used, the formula calculation uses existing functionality.

## Using TCA for coproducts
Here are some of the guidelines for using TCA for co-products:

-   If you set the **Total Cost Allocation** slider to **Yes** for a formula version, co-products must have a cost price that is more than 0 (zero). The value can be retrieved from the active cost version for the same site, or for the first site for a formula that isn't site-specific. This condition is validated when the formula is approved.
-   If you set the **Total Cost Allocation** slider to **Yes** for the formula version and the following conditions are true, the method of cost allocation is **TCA**, and the percentage of cost allocation is unchanged:
    -   You added co-products.
    -   You used a different method of cost allocation for the co-products.
-   If you set the **Total Cost Allocation** slider to **No** for the formula version and the following conditions are true, the method of cost allocation is changed to **Manual**, and the percentage of cost allocation is unchanged:
    -   You added co-products.
    -   The percentage of cost allocation is more than 0 (zero).
-   Before you can successfully perform a formula calculation, you must estimate the percentages of cost allocation. You can complete this step either manually or by using the **Estimate cost** option on the **Co-products** page. **Note:** The **Estimate cost** option is available only when the **Total Cost Allocation** slider is set to **Yes** for the formula version. You can view the expected allocation if the batch order quantities that are reported as finished match quantities that appear on the formula.
-   When a batch order is created manually or a planned batch order is firmed, the value of the **Total Cost Allocation** slider for the formula version is copied to the batch order. However, you can change this setting on the batch order. If the **Total Cost Allocation** slider is set to **No** for the formula version and then changed to **Yes** for the batch order, the method of cost allocation for each line that was set to **Manual** is changed to **TCA**. A cost allocation of **None** is unchanged. If the **Total Cost Allocation** slider is set to **Yes** for the formula version and then changed to **No** for the batch order, the method of cost allocation for each co-product of the **Production** type is changed to **Manual**. Any estimated percentage of cost allocation is unchanged.
-   The **Co-product cost allocation** page shows the calculated cost allocation percentage. You can open this page from the **Batch order** page. This information is useful when the products and quantities that are reported differ from the scheduled or started quantities on the batch order. When the cost is complete, these new percentage allocations from TCA are shown on the **Co-product cost allocation** page.

## Calculating the burden for byproducts
The **By-product cost allocation** field on the **Co-products** page is an enumerator field that is used only for by-products. For co-products, the value of this field is always **None**. For by-product lines, this field determines how the cost amount for the by-product line is added to the total cost of the production. The following options are available:

-   **None** ─ No amount is added to the total cost of the production for this by-product line.
-   **Percent** ─ The cost amount is calculated as a percentage of the total cost of raw materials that are consumed in the production. The percentage that is used for the calculation is entered in the field.
-   **Per series** ─ The cost amount is calculated as an amount per standard batch size of the production order. This amount is independent of the reported quantity in the production. The amount that is used for the calculation is entered in the field.
-   **Per quantity** ─ The cost amount is calculated as an amount per reported quantity of the formula item in the production. The amount that is used for the calculation is entered in the field.

