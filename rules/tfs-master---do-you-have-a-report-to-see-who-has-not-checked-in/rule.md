---
type: rule
title: TFS Master - Do you have a report to see who has not checked in?
uri: tfs-master---do-you-have-a-report-to-see-who-has-not-checked-in
created: 2011-11-18T03:52:29.0000000Z
authors:
- id: 22
  title: David Klein
- id: 5
  title: Justin King
- id: 17
  title: Ryan Tee
- id: 6
  title: Tristan Kurniawan
related: []

---

Managers should regularly check to see if developers are committing their changes into source control. In TFS you can only get a status by manually looking at each project or running "tfs status" command. A great tool is [Attrice Team Foundation SideKicks](http://visualstudiogallery.msdn.microsoft.com/c255a1e4-04ba-4f68-8f4e-cd473d6b971f) which can display the status of all users and projects
 
![Use TFS Sidekicks and search for files older than 48 hours to find the naughty boys. Suggestion for TFS Sidekicks: Add a button to “Email all people their shame list”…. showing their files that are still checked out](SideKicksStatus.jpg)(until then I do it manually)