---
type: rule
archivedreason: 
title: Do use spaces in table names?
guid: c9d05912-2642-4577-8848-fff9188217c1
uri: do-use-spaces-in-table-names
created: 2010-07-22T05:09:16.0000000Z
authors:
- id: 1
  title: Adam Cogan
related:
- do-you-have-hidden-tables-or-queries-upsizing-problem
- do-you-use-underscores-preference-only
- do-you-always-have-a-unique-index-on-a-table

---

Having spaces in table names necessitates the use of square brackets in all your code. e.g. [Order Details].[Order ID] instead of OrderDetail.OrderID. Spaces will also cause problems when you upsize to SQL Server later on... there is just no benefit.
<font class="ms-rteCustom-YellowBorderBox"><a href="http&#58;//www.ssw.com.au/ssw/UpsizingPRO">Upsizing PRO</a> will check this rule </font>
<!--endintro-->