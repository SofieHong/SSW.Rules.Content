---
type: rule
archivedreason: 
title: Do you use jQuery for making a site come alive?
guid: 27612f09-8114-4b19-b7c3-66f172c94a15
uri: do-you-use-jquery-for-making-a-site-come-alive
created: 2009-08-25T00:13:02.0000000Z
authors:
- id: 1
  title: Adam Cogan
related: []

---

To please customers every business knows they need to keep their services and offerings fresh and up-to-date. The same is true for websites. In order to attract new traffic, we should make the website vivid.   
<!--endintro-->
<dl class="badImage">    &lt;dt&gt;<img alt="Bad example – there is no response when mouse is over the image" src="OldFashionSite.jpg"> &lt;/dt&gt;
    <dd>Figure: Bad example – there is no response when mouse is over the image </dd></dl><dl class="goodImage">    &lt;dt&gt;<img alt="Good example – apply the different style when mouse is over" src="NewFashionSite.jpg"> &lt;/dt&gt;
    <dd>Figure: Good example – apply the different style when mouse is over </dd></dl><dl class="goodCode">    &lt;dt&gt;
    <pre>        
        $("p").hover(function () {
            $(this).css({ "background-color":"yellow", "font-weight":"bolder" }); },
            function () { 
                var cssObj = { "background-color": "#ddd", 
                "font-weight": "", 
                color: "rgb(0,40,244)"
            }
            $(this).css(cssObj);
        }); 
    </pre>
    &lt;/dt&gt;
    <dd>Figure: Mouse hover sample </dd></dl>