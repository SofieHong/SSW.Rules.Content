---
type: rule
archivedreason: 
title: Do you know how to laser in on the smelliest code?
guid: c69ca2e5-0323-430e-ae26-62a753d4ace5
uri: do-you-know-how-to-laser-in-on-the-smelliest-code
created: 2012-03-16T08:36:31.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 23
  title: Damian Brady
- id: 24
  title: Adam Stephensen
related: []

---

Rather than randomly browsing for dodgy code, use Visual Studio's Code Metrics feature to identify "Hot Spots" that require investigation.
<dl class="badImage">&lt;dt&gt; 
      <img alt="467510-lotto-balls.jpeg" src="lotto-balls.jpeg" style="width:600px;"> 
   &lt;/dt&gt;<dd>Figure: The bad was is to browse the code<br></dd></dl>
<!--endintro-->
<dl class="image">&lt;dt&gt;
      <img src="VS 11 Code Metrics.png" alt="Run Code Metrics">
   &lt;/dt&gt;<dd>Figure: Run Code Metrics in Visual Studio</dd></dl><dl class="image">&lt;dt&gt;
      <img src="CodeMetrics_3.png" alt="Red dots indicate the code that is hard to maintain" style="width:750px;height:389px;">
   &lt;/dt&gt;<dd>Figure: Red dots indicate the code that is hard to maintain. E.g. Save() and LoadCustomer()</dd></dl>
Identifying the problem areas is only the start of the process. From here, you should speak to the developers responsible for this dodgy code. There might be good reasons why they haven't invested time on this.
<dl class="image">&lt;dt&gt;
      <img class="ms-rteCustom-ImageArea" src="codelens-start-conversation.png" alt="codelens-start-conversation.png">  
      <br>
   &lt;/dt&gt;<dd>Figure: Find out who the devs are by using CodeLens and start a conversation<span style="color:#444444;"></span></dd></dl> **Tip:** To learn how to use Annotate, see  [Do you know the benefits of Source Control?](http://www.ssw.com.au/ssw/Standards/Rules/RulesToBetterSourceControlwithTFS.aspx#UsingSourceControl)




::: greybox
**Suggestion to Microsoft:** allow us to visualize the developers responsible for the bad code (currently and historically) using CodeLens.

:::