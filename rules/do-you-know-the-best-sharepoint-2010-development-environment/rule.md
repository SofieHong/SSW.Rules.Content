---
type: rule
archivedreason: 
title: Do you know the best SharePoint 2010 development environment?
guid: 14e60294-7eb5-436b-b8c6-aff34f0a3d70
uri: do-you-know-the-best-sharepoint-2010-development-environment
created: 2009-12-15T06:34:40.0000000Z
authors:
- id: 8
  title: John Liu
- id: 1
  title: Adam Cogan
- id: 14
  title: Martin Hinshelwood
related: []

---

Developing in ASP.NET is easy, you just press F5, Visual Studio spins up instance of the Cassini web server, and you can see your work execute. Developing in SharePoint is much harder as you need access to a local SharePoint server to see your work run.

In SharePoint 2007 there are three options, in SharePoint 2010 they have added one more.

![](SetupSPEnviroment.jpg) <font class="ms-rteCustom-FigureNormal">Figure: Setting up the development environment in SharePoint can give you a headache</font>
<!--endintro-->
 Your development choices in SharePoint 2007 are: 
* Remote to a shared SharePoint development server 
<br>    Tip: This is best for people who do \*not\* need to have their own SharePoint server, such as designers, testers or content editors.
<br>    Problem #1: By default you only get 2 concurrent accounts
<br>    Problem #2: IISRESET clobbers other users.
* Run your own local virtual machine (VM)
<br>    Tip #1: Use an external drive to make it faster
<br>    Tip #2: Use SSD to go even faster :)
* Use ‘Boot’ to VHD (Recommended - most trouble but best performance)
<br>    Note: Only if you have Windows 7 as the host 
<br>    See: [Less Virtual, More Machine - Windows 7 and the magic of Boot to VHD](http://www.hanselman.com/blog/LessVirtualMoreMachineWindows7AndTheMagicOfBootToVHD.aspx)


One of the biggest problem is that SharePoint 2007 can only be installed on Windows Server and most developer machines do not run Windows Server as the host OS. Tweaks to install SharePoint to Vista were available, but considered risky – since your development environment does not fully reflect the production server.
 In SharePoint 2010 – the scenery has changed a little. These are all your options now:

* Remote to a shared SharePoint development server 
<br>    Tip: This is best for people who do \*not\* need to have their own SharePoint server, such as designers, testers or content editors.
<br>    Problem #1: By default you only get 2 concurrent accounts
<br>    Problem #2: IISRESET clobbers other users.
* Run your own local virtual machine (Not recommended – because SharePoint 2010 is 64-bit only) 
<br>    Tip #1: Use an external drive to make it faster
<br>    Tip #2: Use SSD to go even faster :)
<br>    Tip #3: The 64-bit requirement means, you can’t use Virtual PC, and so you have to use either Hyper-V (which requires a Windows Server host), or VMWare
<br>    Tip #4: The 64-bit requirement means, your host must be x64 to run the virtual machines in x64
* Use ‘Boot’ to VHD (Recommended) 
<br>    Note: Only if you have Windows 7 as the host
<br>    See: [Less Virtual, More Machine - Windows 7 and the magic of Boot to VHD](http://www.hanselman.com/blog/LessVirtualMoreMachineWindows7AndTheMagicOfBootToVHD.aspx)
* Install SharePoint 2010 on your Windows 7 PC (Not Recommended)
<br>    You are not fully representing the production server

 Are there any shortcuts for Silverlight developers (for SharePoint consumption)? 

* Yes, you can easily deploy a xap file to a document library. However, if you need to debug it you will need the SharePoint 2010 object model. 
<br>    Tip: You could minimise your exposure to the object model by using a Repository pattern, which would allow you to debug and test your application without SharePoint, but ultimately you will need to debug and test in SharePoint.


![](UltimateSolution.jpg) <font class="ms-rteCustom-FigureNormal">Figure: The Ultimate solution for SharePoint development environments is to have another machine under your desk.</font> The Ultimate Solution 

* Get yourself a second machine (same as remote)
* But don’t share it with anyone else!