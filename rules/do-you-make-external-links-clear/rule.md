---
type: rule
archivedreason: 
title: Do you make external links clear?
guid: d178549e-bdef-4636-8dc7-b3514b360bd0
uri: do-you-make-external-links-clear
created: 2015-02-16T02:21:22.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 16
  title: Tiago Araujo
related: []

---

When creating links, you should follow a few basic rules:

<!--endintro-->

1. If your link is an internal link, then it should navigate within the same window. If the link is external, it should open in a new tab and be visually clear to the user that it will lead them away from the current site, that way it is not a surprise.
2. If a link is to an external site, a <br>       **visual indication** should be provided to the user like this: <br>      [This is a link to another site](http&#58;//www.ssw.com.au/ssw/Redirect/Microsoft/microsoft.htm). <br>      <dl class="badImage"><br><br>::: greybox<br>Search Engines (<a class="ignore" href="http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm" target="_blank">http&#58;//www.google.com</a> is by far the best but try other search engines as well)<br>:::<br><br><dd>Figure&#58; Bad example - Without visual indication</dd></dl><dl class="goodImage"><br><br>::: greybox<br>Search Engines (<a href="http&#58;//www.ssw.com.au/ssw/Redirect/Web/Google.htm" target="_blank">http&#58;//www.google.com</a>&#160;is by far the best but try other search engines as well<br>:::<br><br><dd>Figure&#58; Good example - With visual indication<br></dd></dl>
3. External link <br>       **external indicators should be inserted by CSS** as following: <br>      <dl class="goodImage"><p class="ssw15-rteElement-CodeArea">a[href*=&quot;//&quot;]&#58;not([href*=&quot;mysite.com&quot;])&#58;after &#123; 
            <br>&#160; &#160; content&#58; url(https&#58;//www.ssw.com.au/ssw/images/external.gif); 
            <br>&#160; &#160; padding-left&#58; 4px;<br>&#125;</p><dd>Figure&#58; Good example - Icon is added by CSS via a simple declaration<br></dd></dl>


We have a program called     [SSW Code Auditor](http&#58;//www.ssw.com.au/ssw/CodeAuditor/) to check for this rule.
 


### Related Rule <br>      


* [Do you make external links open on a new tab?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&amp;TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&amp;TermId=1d8a7afd-9762-4bfd-971c-cacd787c28bb)