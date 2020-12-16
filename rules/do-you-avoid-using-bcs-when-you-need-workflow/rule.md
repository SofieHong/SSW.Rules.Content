---
type: rule
archivedreason: 
title: Do you avoid using BCS when you need Workflow?
guid: 3ded0c3f-ba49-4b56-9b40-4e85c8f1472c
uri: do-you-avoid-using-bcs-when-you-need-workflow
created: 2010-06-04T06:39:12.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []

---

If you are planning to use Workflow, use Workflow with SharePoint List instead of BCS. Because Workflow cannot be associated directly with external lists. The reason is data is not stored in SharePoint, so the Workflow cannot be notified when items change.

<!--endintro-->



![](BCSDoesNotSupportWF.jpg)
<font class="ms-rteCustom-FigureBad">BCS doesn't have WorkFlow support<br></font>


![](WFSupportList.jpg)
<font class="ms-rteCustom-FigureGood">Use WorkFlow with SharePoint List</font>