---
type: rule
archivedreason: 
title: Do you use Asynchronous method and CallBack when invoke web method?
guid: 2be94004-f384-49cc-bd12-8a7428ecf585
uri: do-you-use-asynchronous-method-and-callback-when-invoke-web-method
created: 2009-05-13T07:06:50.0000000Z
authors:
- id: 1
  title: Adam Cogan
- id: 17
  title: Ryan Tee
related: []

---

Web service and web invoking becomes more and more popular today as the distributed systems are widely deployed. However, the normal method invoking may cause a disaster when apply to web method because transmitting data over Internet may cause your program to hang for a couple of minutes.   
<!--endintro-->
<dl class="badCode">    <dt style="width:91.56%;height:174px;">private static string LoadContentFromWeb(string strUri) <br>
    <br>
    { <br>
    ... <br>
    <br>
    <span style="background-color:#ffff00;">WebResponse response = request.GetResponse(); </span><br>
    <br>
    ...<br>
    } &lt;/dt&gt;
    <dd>Figure: Invoke web method by the normal way (Bad - because this will hang your UI thread) </dd></dl>
The correct way to invoke web method is using asynchronous call to send a request and use the delegated CallBack method to read the response, see code below:
<dl class="goodCode">    <dt style="width:91.4%;height:660px;"> public static void GetOnlineVersionAsync(string strUri) <br>
    { <br>
        try<br>
        {<br>
         ...<br>
    <br>
            <span style="background-color:#ffff00;">IAsyncResult r = request.BeginGetResponse(new AsyncCallback(ResCallBack), request);</span><br>
         }<br>
         catch(WebException ex)<br>
        {<br>
            Console.WriteLine(ex.ToString()) ; <br>
         }<br>
    }<br>
    <br>
    <br>
    <br>
    private static void ResCallBack(IAsyncResult ar)<br>
    {<br>
       try<br>
       {<br>
    <span style="background-color:#ffff00;">      string content = string.Empty;<br>
          WebRequest req = (WebRequest)ar.AsyncState;<br>
          WebResponse response = req.EndGetResponse(ar);</span><br>
    <br>
          ...<br>
    <br>
          RaiseOnProductUpdateResult(content);<br>
    <br>
       }<br>
       catch(WebException ex)<br>
       {<br>
          Console.WriteLine(ex.ToString());<br>
          RaiseOnProductUpdateResult(string.Empty);<br>
        }<br>
    } &lt;/dt&gt;
    <dd>Figure: Invoke web method by using asynchronous method and CallBack (Good - UI thread will be free once the request has been sent) </dd></dl>
When working with Web Service, asynchronous methods will be automatically generated by your web services proxy.
<dl class="image">    &lt;dt&gt;<img alt="" style="border-bottom:0px solid;border-left:0px solid;border-top:0px solid;border-right:0px solid;" border="0" src="AsyncCallBack-Rulest1.gif"> &lt;/dt&gt;
    <dd>Figure: Automatically generated asynchronous methods</dd></dl>