---
type: rule
archivedreason: 
title: Do you catch and re-throw exceptions properly?
guid: d8992617-dcae-4dca-b775-9e417507d1b5
uri: do-you-catch-and-re-throw-exceptions-properly
created: 2013-09-11T21:16:44.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 38
  title: Drew Robson
related: []

---

A good catch and re-throw will make life easier while debugging, a bad catch and re-throw will ruin the exception's stack trace and make debugging difficult.

<!--endintro-->
<dl class="bad">&lt;dt&gt;<pre>catch &#123;&#125; 
<span style="color&#58;#ff0000;">(Never use an empty catch block. Do something in the block or remove it.)</span>

catch (SomeException) &#123;&#125; 
<span style="color&#58;#ff0000;">(Never use an empty catch block. Do something in the block or remove it.)</span>

catch &#123; throw; &#125; 
<pre><span style="color&#58;#ff0000;">(Never use an empty catch block. Do something in the block or remove it.)</span></pre>
catch (SomeException) &#123; throw; &#125; 
<pre><span style="color&#58;#ff0000;">(Never use an empty catch block. Do something in the block or remove it.)</span></pre>
catch (SomeException ex) &#123; throw ex; &#125; 
<span style="color&#58;#ff0000;">(Never re-throw exceptions by passing the original exception object. Wrap the exception or use throw; instead.)</span>

catch (SomeException ex) &#123; someMethod(); throw ex; &#125; 
<span style="color&#58;#ff0000;">(Never re-throw exceptions by passing the original exception object. Wrap the exception or use throw; instead.)
</span>
</pre>&lt;/dt&gt;<dd>Bad Example - Bad code</dd></dl><dl class="good">&lt;dt&gt;<pre>catch (SomeException ex) 
&#123; 
     someMethod(); 
     throw; 
&#125;

catch (SomeException ex) 
&#123; 
     someMethod(); 
     SomeOtherException wrapperEx = new SomeOtherException(&quot;This is a wrapper exception&quot;, ex);
     throw wrapperEx; 
&#125;
</pre>&lt;/dt&gt;<dd>Good Example - Good code</dd></dl>
We have a program called [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/Default.aspx) to check for this rule.