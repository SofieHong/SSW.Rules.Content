---
type: rule
archivedreason: 
title: Do you reply to the correct Zendesk email?
guid: 05e79060-8a83-4d49-b9e1-2c5831307637
uri: do-you-reply-to-the-correct-zendesk-email
created: 2018-06-28T23:13:36.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 73
  title: Kaique Biancatti
related: []

---

When a ticket is created in Zendesk, an email for it is created as well - and, if you have set up Zendesk correctly, the correct group of people will already receive the task.

<!--endintro-->

In Zendesk, you can set groups, like 'SysAdmins' and 'Sales'and insert the correct people there already, so there is no need to add another group of the same people to the email. That is repetition and it is not necessary.

For example, Zendesk is set up with the email SysAdmins@ssw.zendesk.com and there is a group called SysAdmin@ssw.com.au. The former is a Zendesk group to manage tasks, the latter is a mail distribution group, and both groups got the same people in it.

It is best practice to only use the Zendesk group to manage tasks and not both groups in the same email thread.


![](zenddddd.png)


::: bad
Bad Example: Adding groups with the same people twice. They will receive it twice in their inbox

:::





![](zendndnd.png)


::: good
Good Example: Add only one group, that goes to Zendesk and spread the ticket only once for everyone

:::




### Related Links


* [Rules to Better Scrum - Do you know when to use @ mentions in a PBI](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=efd6c91e-7cc5-4473-a299-9104c8fd6e0d)