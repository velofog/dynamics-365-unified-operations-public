---
# required metadata

title: X++ language reference
description: This topic provides programming guidance for X++.
author: RobinARH
manager: AnnBe
ms.date: 2016-03-29 19 - 23 - 25
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 

# optional metadata

# ms.search.form: 
# ROBOTS: 
audience: Developer
# ms.devlang: 
# ms.reviewer: 61
ms.search.scope: AX 7.0.0, Operations
# ms.tgt_pltfrm: 
ms.custom: 72181
ms.assetid: 5cf3c224-b05e-4f3a-95eb-ebfa18b1b0bd
ms.search.region: Global
# ms.search.industry: 
ms.author: robinr
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0

---

# X++ language reference

This topic provides programming guidance for X++.

X++ is an object-oriented, application-aware, and data-aware programming language that Microsoft Dynamics AX uses in enterprise resource planning (ERP) programming and in database applications. It provides system classes for a broad range of system programming areas, highlighted in the following table.
|                             |                                                                                                                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **X++ language attributes** | **Description**                                                                                                                                                                      |
| **Classes**                 | In addition to system classes, Microsoft Dynamics AX also provides application classes for managing many types of business processes. Reflection on classes is supported.            |
| **Tables**                  | X++ programmers can access the relational tables in Microsoft Dynamics AX. X++ includes keywords that match most of the keywords in standard SQL. Reflection on tables is supported. |
| **User interface**          | Manipulation of user interface items, such as forms and reports.                                                                                                                     |
| **Best practice checks**    | X++ code is checked for syntax errors during compile time. The compile process also performs best practice checks. Violations of best practices can generate compiler messages.      |
| **Garbage collection**      | The X++ runtime execution engines have automatic mechanisms to discard objects that are no longer referenced, so that memory space can be reused.                                    |
| **Interoperability**        | Microsoft Dynamics AX supports interoperability between classes written in X++ and in C\# (or other .NET Framework languages).                                                       |
| **File manipulation**       | File input and output is supported, including XML building and parsing.                                                                                                              |
| **Collections**             | Dynamic arrays are supported and the X++ includes several collection objects.                                                                                                        |

The X++ language programming guide is divided into these sections: [X++ attribute classes](xpp-attribute-classes.md) [X++ classes and methods](xpp-classes-methods.md) [X++ data selection and manipulation](xpp-data-query.md) [X++ macros](macros-xpp.md) [X++ operators](xpp-operators.md) [X++ statements and loops](xpp-statements-loops.md)[X++ variables and data types](xpp-variables-data-types.md)

See also
--------

[X++ Syntax](xpp-syntax.md)

[X++ and C# Comparison](xpp-cs-comparison.md)
