---
type: rule
archivedreason: 
title: Do you add Web Tests to Application Insights to monitor trends over time?
guid: 5e6bd24c-5137-454c-bc32-3aceb6b253d8
uri: do-you-add-web-tests-to-application-insights-to-monitor-trends-over-time
created: 2015-09-02T09:09:08.0000000Z
authors:
- id: 45
  title: Chris Briggs
related: []

---

As soon as you have configured Application Insights, you should immediately add a Web Test to track general performance trends over time. You can configure test agents to access your application from different locations around the globe to give a general idea of what users will experience.

<!--endintro-->

Instructions on how to add Web Tests can be found on MSDN [https://azure.microsoft.com/en-us/documentation/articles/app-insights-monitor-web-app-availability](https://azure.microsoft.com/en-us/documentation/articles/app-insights-monitor-web-app-availability/)

Setting up a Web Test will allow you to query and see how the performance of your application has  changed over a period of time and to help you spot any anomalies. It can be useful to query over a long period of time (e.g. a year) and see if the performance has stayed the same or if there have been any regressions in responsiveness.
<dl class="goodImage">&lt;dt&gt; <img alt="App Insights Web Test.png" src="App-Insights-Web-Test.png" style="width:742px;">&lt;/dt&gt;<dd>Good Example - You can clearly see the point where we deployed a fix to production to improve the initial page load. </dd></dl>
You have the ability to drill down into web test results, to get an overview of the response time of the resources on a page. This can help discover if certain resources are slowing the response time.
<dl class="goodImage">&lt;dt&gt; <img alt="App Insights Web Test drilldown.png" src="App-Insights-Web-Test-drilldown.png" style="width:650px;">&lt;/dt&gt;<dd> Good Example - Reviewing the Web test results, provides vital information .</dd></dl>