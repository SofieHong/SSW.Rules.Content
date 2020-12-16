---
type: rule
archivedreason: 
title: Do you create a minimal master page?
guid: 591f621f-a7fb-4ff3-b86d-4ca3fbc085e1
uri: do-you-create-a-minimal-master-page
created: 2009-06-18T06:46:53.0000000Z
authors:
- id: 8
  title: John Liu
- id: 18
  title: Jay Lin
related: []

---

To create a master page or reuse an existing master page is a time-consuming process. Because you have to determine what the Office SharePoint Server 2007 page model requires — necessary content placeholders and controls to work with the page layouts.

 Another problem of Default.master is that it contains many tables that are difficult to style.  
<!--endintro-->
<dl class="badCode"> &lt;dt&gt;&lt;%@Master language=&quot;C#&quot;%&gt;<br>...<br>&lt;HEAD runat=&quot;server&quot;&gt;<br>...<br>&lt;Title ID=onetidTitle&gt;<br>&lt;asp&#58;ContentPlaceHolder id=PlaceHolderPageTitle runat=&quot;server&quot;/&gt;<br>&lt;/Title&gt;<br>...<br>&lt;/HEAD&gt;<br>&lt;BODY scroll=&quot;yes” ... &gt;<br>&lt;form runat=&quot;server&quot; onsubmit=&quot;return _spFormOnSubmitWrapper();&quot;&gt;<br>&lt;WebPartPages&#58;SPWebPartManager id=&quot;m&quot; runat=&quot;Server&quot;/&gt;<br>
    <font style="background-color&#58;#ffff80;">&lt;table class=&quot;ms-main&quot; CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH=&quot;100%&quot; HEIGHT=&quot;100%&quot;&gt;</font><br>&lt;tr&gt;<br>&lt;td&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderGlobalNavigation&quot; runat=&quot;server&quot;&gt;<br>
    <font style="background-color&#58;#ffff80;">&lt;table CELLPADDING=0 CELLSPACING=0 BORDER=0 WIDTH=&quot;100%&quot;&gt;</font><br>...<br>&lt;/table&gt;<br>&lt;/asp&#58;ContentPlaceHolder&gt;<br>&lt;/td&gt;<br>&lt;/tr&gt;<br>&lt;tr&gt;<br>...<br>&lt;/tr&gt;<br>&lt;tr&gt;<br>&lt;td id=&quot;onetIdTopNavBarContainer&quot; WIDTH=100% class=&quot;ms-bannerContainer&quot;&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderTopNavBar&quot; runat=&quot;server&quot;&gt;<br>...<br>&lt;/asp&#58;ContentPlaceHolder&gt;<br>&lt;/td&gt;<br>&lt;/tr&gt;<br>&lt;tr height=&quot;100%&quot;&gt;<br>&lt;td&gt;<br>
    <font style="background-color&#58;#ffff80;">&lt;table width=&quot;100%&quot; height=&quot;100%&quot; cellspacing=&quot;0&quot; cellpadding=&quot;0&quot;&gt;</font><br>...<br>&lt;/table&gt;<br>&lt;/td&gt;<br>&lt;/tr&gt;<br>&lt;/table&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderFormDigest&quot; runat=&quot;server&quot;&gt;<br>...<br>&lt;/asp&#58;ContentPlaceHolder&gt;<br>...<br>&lt;/form&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderUtilityContent&quot; runat=&quot;server&quot;/&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderBodyAreaClass&quot; runat=&quot;server&quot;/&gt;<br>&lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderTitleAreaClass&quot; runat=&quot;server&quot;/&gt;<br>&lt;/BODY&gt;<br>&lt;/HTML&gt;&lt;/dt&gt; <dd>Bad example - using default master page </dd> </dl>
So we recommend using the minimal master page which includes the necessary placeholders.
To create a minimal master page

1. Open SharePoint Designer.
2. On the File menu, click New, point to SharePoint Content, and then click the Page tab.
3. Double-click Master Page to create a new master page.
4. Click Design to show the master page in design view. You should see header and left margin areas and several content placeholders in the master page.
5. Click Code to show the master page in code view.
6. Copy the code into the master page 
SharePoint 2007 - [https://msdn.microsoft.com/en-us/library/office/aa660698(v=office.12).aspx](https&#58;//msdn.microsoft.com/en-us/library/office/aa660698%28v=office.12%29.aspx) 
SharePoint 2010 - [https://msdn.microsoft.com/en-us/library/office/dn205 273.aspx](https&#58;//msdn.microsoft.com/en-us/library/office/dn205273.aspx)
<dl class="goodCode"> &lt;dt&gt;&lt;%@ Master language=&quot;C#&quot; %&gt;<br>...<br>&lt;html&gt;<br>&#160;&#160;&#160; &lt;WebPartPages&#58;SPWebPartManager runat=&quot;server&quot;/&gt;<br>&#160;&#160;&#160; &lt;SharePoint&#58;RobotsMetaTag runat=&quot;server&quot;/&gt;<br>&#160;&#160;&#160; &lt;head runat=&quot;server&quot;&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;ContentPlaceHolder runat=&quot;server&quot; id=&quot;head&quot;&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;title&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderPageTitle&quot; runat=&quot;server&quot; /&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;/title&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;/asp&#58;ContentPlaceHolder&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;Sharepoint&#58;CssLink runat=&quot;server&quot;/&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderAdditionalPageHead&quot; runat=&quot;server&quot; /&gt;<br>&#160;&#160;&#160; &lt;/head&gt;<br>&#160;&#160;&#160; &lt;body onload=&quot;javascript&#58;_spBodyOnLoadWrapper();&quot;&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;form runat=&quot;server&quot; onsubmit=&quot;return _spFormOnSubmitWrapper();&quot;&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;wssuc&#58;Welcome id=&quot;explitLogout&quot; runat=&quot;server&quot;/&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;PublishingSiteAction&#58;SiteActionMenu runat=&quot;server&quot;/&gt; <br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;PublishingWebControls&#58;AuthoringContainer id=&quot;authoringcontrols&quot; runat=&quot;server&quot;&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;PublishingConsole&#58;Console runat=&quot;server&quot; /&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;/PublishingWebControls&#58;AuthoringContainer&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderMain&quot; runat=&quot;server&quot; /&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;Panel visible=&quot;false&quot; runat=&quot;server&quot;&gt;<br>&#160;&#160;&#160; &#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;asp&#58;ContentPlaceHolder id=&quot;PlaceHolderSearchArea&quot; runat=&quot;server&quot;/&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &#160;&#160;&#160;&#160;&#160;&#160;&#160; ...<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&#160;&lt;/asp&#58;Panel&gt;<br>&#160;&#160;&#160;&#160;&#160;&#160;&#160; &lt;/form&gt;<br>&#160;&#160;&#160; &lt;/body&gt;<br>&lt;/html&gt;&lt;/dt&gt; <dd>&#160;&#160;&#160; Good example - using minimal master page </dd> </dl>
7. On the File menu, click Save As, provide a unique file name with the .master extension, and then save the file to the master page gallery (/\_catalogs/masterpage) in your site collection.