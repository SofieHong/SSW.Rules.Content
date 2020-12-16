---
type: rule
archivedreason: 
title: Do you know how to work with document versions?
guid: 976fe4d1-ecfa-41c8-b597-e22cb7bd6b81
uri: do-you-know-how-to-work-with-document-versions
created: 2009-07-23T03:16:53.0000000Z
authors:
- id: 8
  title: John Liu
- id: 1
  title: Adam Cogan
related: []

---

This is how you should work with Document Versions: 
<!--endintro-->

1. Make sure your document library is configured to use versioning.
 TIP: You can configure this in Settings | Versioning Settings
2. Make sure you are showing the version column in your document view. <br>      <dl class="image">&lt;dt&gt;
            <img border="0" src="VersionColumn_Small.jpg" alt="Add a version column" style="border-width:0px;border-style:solid;">
         &lt;/dt&gt;</dl>    TIP: You can add the column by selecting Modify View
3. Whenever you edit the document and check it in, SharePoint will automatically increase the version number.
    If you need to send this document to a client then it is important to:
    1. Save the file locally by selecting Send To | Download a Copy <br>         <dl class="image">&lt;dt&gt;
               <img border="0" src="SaveFileLocally_Small.jpg" alt="Save a file locally">
            &lt;/dt&gt;</dl>
    2. Add the version to the end of the filename e.g. Specifications\_v2.0.docx
    3. Then email it to the client.
    4. We do this so that we can track what version of the document was sent to the client.
        TIP: If you are not working with SharePoint then we recommend you follow the rule           [Do you include version numbers in your file names?](http://www.ssw.com.au/ssw/Standards/Rules/RulesToBetterTechnicalDocumentation.aspx#VersionNumber)