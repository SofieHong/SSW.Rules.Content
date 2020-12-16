---
type: rule
archivedreason: 
title: Do you use Html Helpers and Partial Views to simplify Views?
guid: 13fd4eb4-925e-47c1-b779-c54b9b869385
uri: do-you-use-html-helpers-and-partial-views-to-simplify-views
created: 2013-03-07T18:47:43.0000000Z
authors:
- id: 23
  title: Damian Brady
related: []

---

Repeated sections of User Interface should be encapsulated in either Html Helpers or Partial Views to avoid repetition.

<!--endintro-->
<dl class="badImage">&lt;dt&gt;<br><br>::: greybox<br><pre>&lt;div class=&quot;featured&quot;&gt;
    @if (ViewData.ContainsKey(&quot;FeaturedProduct&quot;))
    &#123;
        &lt;span class=&quot;ProductName&quot;&gt;@ViewBag.FeaturedProduct.Name&lt;/span&gt;
        &lt;span class=&quot;ProductPrice&quot;&gt;@ViewBag.FeaturedProduct.Price&lt;/span&gt;
    &#125;
&lt;/div&gt;

</pre><br>:::<br><br>&lt;/dt&gt;<dd>Figure&#58; Bad Example – The above code could be encapsulated into a Partial View for reuse</dd></dl><dl class="goodImage">&lt;dt&gt;<br><br>::: greybox<br><pre>public static class DateExtensions
&#123;
    public static MvcHtmlString GetTodayDate(this System.Web.Mvc.HtmlHelper helper)
    &#123;
        return new MvcHtmlString(DateTime.Now.ToShortDateString());
    &#125;
&#125;
@Html.GetTodayDate()
</pre><br>:::<br><br>&lt;/dt&gt;<dd>Figure&#58; Good Example – Using an HTML Helper extension method for reusable code</dd></dl><dl class="goodImage">&lt;dt&gt;<br><br>::: greybox<br><pre>@Html.Partial(&quot;_FeaturedProduct&quot;)
</pre><br>:::<br><br>&lt;/dt&gt;<dd>Figure&#58; Good Example – Using a Partial View for reusable sections of UI</dd></dl>