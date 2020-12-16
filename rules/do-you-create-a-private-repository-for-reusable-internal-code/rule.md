---
type: rule
archivedreason: 
title: Do you create a private repository for reusable internal code?
guid: 363bc9b0-d5f7-4ea6-b318-d8f7140628a1
uri: do-you-create-a-private-repository-for-reusable-internal-code
created: 2014-11-27T18:57:56.0000000Z
authors:
- id: 34
  title: Brendan Richards
related: []

---

Nuget is great for managing publicly available packages, but it’s also surprisingly easy to create and publish your own packages to your own nuget server for internal code reuse across multiple solutions.

<!--endintro-->
<dl class="image">&lt;dt&gt; 
      <img src="private-nuget-1.png" alt="private-nuget-1.png" style="width:600px;"> &lt;/dt&gt;<dd>Figure: You can create your own nuget server by simply creating a new asp.net web project and adding the Nuget.Server package</dd></dl><dl class="image">&lt;dt&gt; 
      <img src="private-nuget-2.png" alt="private-nuget-2.png" style="width:600px;">
   &lt;/dt&gt;<dd>Figure: Add your new server as a package source under Tools | Options | Nuget Package Manager | Package Sources</dd></dl>