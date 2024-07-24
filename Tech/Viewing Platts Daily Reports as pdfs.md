Platts used to email pdf attachments of *Platts Gas Daily*, *Platts MW Daily*, *Platts LNG Daily*, etc. Subscribers would then forward these emails to non-subscribers, so Platts became more strict with their access model.

In this brief note, we describe how to open the Platts daily reports as pdfs in Adobe Acrobat. Presumably, this will make it easier to view the reports, integrate their content into our document search tool, integrate with AI tools (if/when approved by the company), etc.
##### Market Reports Webpage
[Platts Connect: Reports (spglobal.com)](https://plattsconnect.spglobal.com/#platts/rptsSearch?reportType=Market%20Reports)
![[Platts Connect Market Reports.png]]

Clicking on the "pdf" icon in the "Actions" column downloads the pdf file.
##### Adobe Acrobat Settings
We have experienced an error when trying to open the downloaded Gas Daily pdf in Adobe Acrobat. Below, we describe the fix:

1. Navigate to "Preferences."
2. Click on the "JavaScript" category.
3. Ensure that the "Enable global object security policy" within the "JavaScript Security" section is *unchecked*.

![[Preferences.png]]
![[Uncheck highlighted box.png]]