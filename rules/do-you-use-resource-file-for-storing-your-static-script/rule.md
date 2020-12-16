---
type: rule
archivedreason: 
title: Do you use resource file for storing your static script?
guid: 826a38d4-86e2-4e68-9809-643454ed2f48
uri: do-you-use-resource-file-for-storing-your-static-script
created: 2009-05-06T09:48:28.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee
related: []

---

Write a Intro pragraph here  
<!--endintro-->

##  
<dl class="badCode">    <dt style="width:92.31%;height:190px;">
    <pre>     StringBuilder sb = new StringBuilder();<br>     sb.AppendLine(@"<script type="" text/javascript""="">");<br>     sb.AppendLine(@"function deleteOwnerRow(rowId)");<br>     sb.AppendLine(@"{");<br>     sb.AppendLine(string.Format(@"{0}.Delete({0}.<br>        GetRowFromClientId(rowId));", OwnersGrid.ClientID));<br>     sb.AppendLine(@"}");<br>     sb.AppendLine(@"</script>"); </pre>
    &lt;/dt&gt;
    <dd>Bad example - Hard to read ?the string is surrounded by rubbish + inefficient because you have an object and 6 strings</dd></dl>

<dl class="goodCode">    <dt style="width:93.08%;height:100px;">
    <pre>     string.Format(@"<script type="" text/javascript""="">                  <br>       function deleteOwnerRow(rowId)                    <br>      { {0}.Delete({0}.GetRowFromClientId(rowId)); } </script> ", <br>       OwnersGrid.ClientID);                                    </pre>
    &lt;/dt&gt;
    <dd>Good example Slightly easier to read ?but it is 1 code statement across 10 lines</dd></dl><dl class="goodCode">    <dt style="width:92.33%;height:86px;">
    <pre>     string scriptTemplate = Resources.Scripts.DeleteJavascript;<br>     string script = string.Format(scriptTemplate, OwnersGrid.ClientID); </pre>
    &lt;/dt&gt;
</dt></dl><dl class="goodCode">    <dt style="width:91.4%;height:161px;">
    <pre>     <script type="" text/javascript""=""><br>     function deleteOwnerRow(rowId)<br>     {<br>            {0}.Delete({0}.GetRowFromClientId(rowId));<br>     }<br>     </script> </pre>
    &lt;/dt&gt;
</dt></dl>
**Figure: The code in the first box, the string in the resource file in the 2nd box. This is the easiest to read + you can localize it eg. If you need to localize an Alert in the javascript**
<dl class="image">    &lt;dt&gt;<img style="border-bottom:0px solid;border-left:0px solid;border-top:0px solid;border-right:0px solid;" border="0" alt="Create a Resource file" src="CreateResource_small.jpg"> &lt;/dt&gt;
    <dd>Figure: Add a recourse file into your project in VS2005</dd></dl><dl class="image">    &lt;dt&gt;<img style="border-bottom:0px solid;border-left:0px solid;border-top:0px solid;border-right:0px solid;" border="0" alt="Create a Resource file" src="ReadResource_small.jpg"> &lt;/dt&gt;
    <dd>Figure: Read value from the new added resource file</dd></dl>