---
type: rule
archivedreason: 
title: Do you use the Code Health Extensions in VS Code?
guid: ba1170f1-3d1a-4af1-b35e-b0c82b5b6ac2
uri: do-you-use-the-code-health-extensions-in-vs-code
created: 2017-03-09T22:12:04.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 46
  title: Danijel Malik
related: []

---

For lightweight web projects such as Angular, often VS Code is more appropriate than Visual Studio. So make sure your code quality remains consistent with CssLint and TSLint.

<!--endintro-->

### Related Steps to Code Health: 


* [Do you use the Code Health Extensions in Visual Studio?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=9e155c90-0502-447a-a1a3-fb2b1580982a)
* [Do you run the Code Health checks in your VisualStudio.com Continuous Integration Build?](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=3c2f0b76-038b-47c2-a754-f897f9d502ef)


### Which Extensions to Use in VS Code


For web projects, we advocate the use of CSSLint for css files and TSLint for typescript files. ([Why you should be using TypeScript instead of JavaScript](/_layouts/15/FIXUPREDIRECT.ASPX?WebId=3dfc0e07-e23a-4cbb-aac2-e778b71166a2&TermSetId=07da3ddf-0924-4cd2-a6d4-a4809ae20160&TermId=d82703e0-6244-4fb6-9017-bac4e4b2361d))
Linters for these can be easily added to VS Code via extensions.
Simply select the "Extensions" tab, search for "CSSLint" and "TSLint" and click "Install" on each respectively.
<dl class="image">&lt;dt&gt;<img src="VSCode-Extensions.png" alt="VSCode-Extensions.png" style="width:650px;">  &lt;/dt&gt;<dd>Figure: Addition of CssLi nt and TSLint to VS Code Project</dd></dl>
If you prefer not to use the Extensions (which are currently a bit out of date). You can install them using npm as normal. 
CssLint ([Csslint npm guide](https://www.npmjs.com/package/csslint))
TSLint ([TSlint npm guide](https://www.npmjs.com/package/tslint))