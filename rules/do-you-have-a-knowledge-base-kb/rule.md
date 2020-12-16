---
type: rule
archivedreason: 
title: Do you have a Knowledge Base (KB)?
guid: 00879668-3bca-40bf-bdeb-7e4970062fc6
uri: do-you-have-a-knowledge-base-kb
created: 2009-03-02T02:45:54.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 27
  title: Titus Maclaren
related: []

---

Do you know what the most useful thing on Microsoft website is? It is their knowledge base at  [http://support.microsoft.com/](http&#58;//support.microsoft.com/)   When a problem arises it should be your first port of call - it allows you to help yourself.  
<!--endintro-->

So, if you answer questions on your products to customers, you are wasting time if you don't have a knowledge base. Just think, you might not be answering Harry's question if he could have looked it up himself.

Now of course there are many customers who don't look for a KB, but instead you fire off the same old email that you already know is an MDAC related error, and your current solution is to tell them to run SSW Diagnostics and get all the green ticks.


::: greybox

Dear Harry,

Thank you for taking the time to report the issue for SSW Code Auditor. I'm happy to let you know that this is a known issue and has been addressed in our knowledge base. 

Please see [http://www.ssw.com.au/ssw/KB/KB.asp?KBID=Q260000](http&#58;//www.ssw.com.au/ssw/KB/KB.asp?KBID=Q260000)

 

Thanks,
John Prince
[<font face="Tahoma">http&#58;//www.ssw.com.au</font>](http&#58;//www.ssw.com.au/ssw/)

:::



::: good
Figure: Responding to a known issue with a KB article
:::


The basic rule is: don't send back the answer in your email - instead send back the link. More specifically:

1. If you can answer a support email then reply to the support email (using one of the 4 templates on the right)
    * TO: the client
    * CC: the developer and your manager with the KB link
2. If you can’t answer the question then reply to the support email
    * TO: the client and the developer
    * CC: your manager
    * Ask the customer if they can get diagnostics to all green ticks.
    * Ask the developer to “Please action?"



::: greybox

Dear Harry,

Thank you for taking the time to report the issue for SSW Code Auditor.

I am sorry to let you know that I cannot reproduce this. Could you please provide me with more details or, even better, would I be able to connect to your PC? It is simple and you can see everything I do. To do so, you can send me an appointment for an appropriate time or add me to your Skype

P.S. Don't forget to run [SSW Diagnostics](http&#58;//www.ssw.com.au/diagnostics), ensuring that you only get green ticks.

Kind Regards, 
Bob

:::



::: good
Figure: Responding when you cannot reproduce the issue
:::



::: greybox

Dear Harry,

Done. The code changed from

xxx
to
     yyy

Thank you for reporting this bug - our software only gets better with help from our customers. This fix will be available in the next version shortly. In the meanwhile, [download an interim build.](http&#58;//www.ssw.com.au/)

Kind Regards,
Bob

:::



::: good
Figure: Informing of a Fix (Email 1 of 2) Note: In this email, you can offer them an interim build
:::



::: greybox

Dear Harry,

Thank you for taking the time to report the issue for SSW Code Auditor. I'm happy to let you know that this problem is fixed in this release.

Please download the new version at [http://www.ssw.com.au/ssw/Download/download.aspx](http&#58;//www.ssw.com.au/ssw/Download/download.aspx)

P.S. Don't forget to run SSW Diagnostics and gets all green ticks [www.ssw.co m.au/diagnostics](http&#58;//www.ssw.com.au/SSW/Diagnostics/default.aspx)

Kind Regards, 
Bob

:::



::: good
Figure: Informing of a New Version (Email 2 of 2)
:::


Notice how by just giving them the URL, this email does the job of encouraging them to use your knowledge base in the future. You need to make sure the support staff know that there are really only 4 types of emails customers should be receiving (see the 4 grey boxes).

Things are running well when you have support staff adding new KB for:

* Known issues
* Hot tips
* Performance tips KBs also play a very important role in getting a product released. You will never get every feature done or bug fixed - we all know it. Focus on getting a version out. It is usually more important to have a version available than having no version at all. When you are looking down the Project Plan, decide on what the \* **must haves** \* are. The others features and known bugs will have to remain outstanding. All the longer term bugs should go into the KB. We also put in the feature requests that we plan on doing. This way our customers know of our exciting features coming in future versions of our software.


However \* **don't** \* write a KB article if fixing the bug and making a new version solves the problem. You'll have to fix the problem anyway, so don't waste time writing a KB, just email the new version. Please see [How to Develop and Reply "Done"](http&#58;//www.ssw.com.au/ssw/extremeemails/default.aspx)

You don't need to be Microsoft to build a KB. A Knowledge Base does not need to be complicated. We use a simple knowledge base which is located at [http://www.ssw.com.au/ssw/KB](http&#58;//www.ssw.com.au/ssw/KB).

Suggestions for features should be added to the backlog and voted on at uservoice.com:


::: greybox

Dear Harry,

Thanks for the suggestion for SSW Code Auditor!

I have added it to the list of future developments (which we call our backlog). Future features can be voted on at [uservoice. com](https&#58;//www.uservoice.com/) .

Thanks,
John Prince

www.ssw.com.au

:::

Figure: Responding to a Feature Suggestion