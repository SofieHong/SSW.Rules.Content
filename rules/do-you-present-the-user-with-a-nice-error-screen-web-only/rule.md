---
type: rule
archivedreason: 
title: Do you present the user with a nice error screen? (Web Only)
guid: 4ee8ca41-78bb-40c1-94cc-cf44a3b47622
uri: do-you-present-the-user-with-a-nice-error-screen-web-only
created: 2013-09-11T21:08:47.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson
related: []

---

Your users should never see the “yellow screen of death” in ASP.NET. Errors should be caught, logged and a user-friendly screen displayed to the user.

<!--endintro-->

This last part is done by specifying the customErrors element in the web.config file.

This will activate ASP.NET’s built in error page (e.g. MVC’s HandleErrorAttribute filter) which can then be customized to suit your application.




> 
![](error-screen-bad.jpg)

<dl class="badImage"><dd>Figure: Bad Example – Yellow Screen of Death</dd></dl><dl class="goodImage">&lt;dt&gt;<img src="error-screen-good.jpg" alt="">&lt;/dt&gt;<dd>Figure: Good Example - Default ASP.NET MVC custom error page</dd><p class="ssw15-rteElement-P"><br></p><p>However, as a developer you still want to be able to view the detail of the exception in your local development environment. Use the below setting in your Web Application's web.config file to view the yellow screen locally but present a nice error screen to the user.<br></p><p></p><p><img src="14-08-2014-2-47-50-PM-compressor.png" alt="14-08-2014-2-47-50-PM-compressor.png" style="margin:5px;width:650px;"><span style="color:#555555;font-size:11px;font-weight:bold;line-height:16px;background-color:transparent;"></span></p><br><br>::: good<br>Figure: Good Example - Don't hide the yellow screen of death in the local environment<br>:::<br><br><p class="ssw15-rteElement-P"><br></p></dl>