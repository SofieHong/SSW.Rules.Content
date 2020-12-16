---
type: rule
archivedreason: 
title: Do you clean useless calendars in SharePoint?
guid: 1e12b128-b34c-4435-af21-81bdef31f061
uri: do-you-clean-useless-calendars-in-sharepoint
created: 2013-09-05T23:49:53.0000000Z
authors:
- id: 9
  title: William Yin
- id: 34
  title: Brendan Richards
related: []

---

Most SharePoint site templates contain a calendar list, this will bring lots of useless calendars.


<!--endintro-->

Use the below PowerShell script to clean them:

$site = Get-SPSite("http://<site collection="" url="">/"); # Specify url here<br>foreach ($web in $site.AllWebs) {    <br>    $lists = $web.Lists<br>    for ($i=($lists.Count-1);$i -gt 0; $i--) {  <br>        $list = $lists[$i]        #Write-host $i  $list.Title $list.BaseTemplate.ToString()<br>        if ($list.BaseTemplate.ToString().ToLower().contains('events')) {      <br>            if ($list.Items.Count -eq 0)<br>            {<br>                Write-Host $list.Items.Count "items in the list" $list.Title '('$list.BaseTemplate') at '$web.Url "- cleaning it!"<br>                $list.Recycle()<br>                #$list.Delete()<br>            }<br>        }<br>    }<br>}  <br></site>

This script will put the calendars which do not have any events into  **Site Settings** |  **Recycle Bin** :
<dl class="ssw15-rteElement-ImageArea"><img src="EmptyCalendarsInRecyckeBin.png" alt="EmptyCalendarsInRecyckeBin.png" style="margin:5px;width:650px;height:236px;"></dl> **Figure: Empty Calendars in Recycle Bin folder**