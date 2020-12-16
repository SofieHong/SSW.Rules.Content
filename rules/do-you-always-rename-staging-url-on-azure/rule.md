---
type: rule
archivedreason: 
title: Do you always rename staging Url on Azure?
guid: 92dd8fc9-110d-4ea6-8340-528f1b1d411e
uri: do-you-always-rename-staging-url-on-azure
created: 2015-03-08T23:23:53.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 47
  title: Stanley Sidik
- id: 43
  title: Michael Demarco
- id: 42
  title: Shigemi Matsumoto
related: []

---

If you use the default Azure staging web site Url, it can be difficult to remember and a waste of time trying to lookup the name every time you access it. Follow this rule to increase your productivity and make it easier for everyone to access your staging site.

<!--endintro-->


| Default Azure Url:<br><ul><li><strong style="line-height:20px;background-color:initial;"> <strong>sugarlearning<span style="color:#ff0066;">-staging</span>.azurewebsites.net</strong> </strong> <br></li></ul> |
| --- |



::: bad
Figure: Bad example - Site using the default Url (hard to remember!!)
:::



| Customized Url:<br><ul><li><strong style="line-height:20px;background-color:initial;"><font color="#ff0066">staging</font></strong> <span style="line-height:20px;background-color:initial;">.</span><strong style="line-height:20px;background-color:initial;">sugarlearning.com</strong> <br></li></ul> |
| --- |



::: good
Figure: Good example - Staging Url having production Url with "staging." prefix
:::




**How to setup a custom Url**

1. Add a CName to the default Url to your DNS server


![CName being added to DNS for the default Url](2015-03-10_17-13-55.png)

2. Instruct Azure to accept the custom Url


![custom domains (1).png](custom domains (1).png)Figure:  Azure being configured to accept the CName