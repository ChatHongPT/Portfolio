---
title: 'Document file forensics (iso modulation)'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - 최홍석

# Author notes (optional)
author_notes:
  - 'BCG Lab undergraduate student'

date: '2024-04-03T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2024-04-03T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication name and optional abbreviated publication name.
publication: In *BCG LABx*
publication_short: In *BCG*

abstract: |
 
  1. Download the Windows.iso file to your desktop.

  2. Mount the Windows.iso file.
  Mounting a Windows.iso file to a virtual drive creates a Windows installation file on that drive (F:).
  Desktop -> Right-click on Windows.iso file -> mount to virtual drive -> (F:) Create ESD-ISO

  3) Check the index number of the desired window version.
  3-1) Because the install.esd file contains different versions of windows, check the index number of the version of window you want to extract.
  3-2) Execute the command prompt as a right holder.
  3-3) Check the index number of the Windows version.
  dism /get-wiminfo/wimfile:F:\sources\install.esd

  4. Extract the wim file.
  4-1) Create a random folder (c:\whs_windows) to generate wim files in advance. 4-2) Extract index: 3 (windows 10 pro).
  4-3) Extract the wim file.
  dism/export0image /sourceimagefile:F:\sources\install.esd /sourceindex:3 /destinationimagefile:c:\whs_windows\install.wim /compress:max

  4-4) Check through the explorer.
  - If you check it in the explorer, you can see that the install.wim file was extracted well in the whs_windows folder. The wim file is also a compressed image file, and the size of the extracted install.wim file is 4.55GB.

  5) Mount the wim through the installed dismgui.

  6) If you open the mounted wim file, you can see the directory structures you often saw in Windows.

  7)Open the Registry Editor.

  8) If malicious code is planted, it is usually planted in HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run. So, I hybridize the software file of the wim file to HKEY_CURRENT_USER.

  9)Find the location of shutdown.exe in cmd through the where command.

  10) Create a shutdown string value in HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run through a registry editor (register value modulation).
  -When you log in to Windows, write data that meets the criteria because the system has to produce malicious code that reboots indefinitely after 5 seconds.
  “C:\Windows\System32\shutdown.exe” /r /f /t 5

  11) Hive offload and do a disout wim.
  - I closed the dismgui during the task practice so I replaced it with the wim folder instead of the whs_windows folder while I was practicing again.

  12)Open windows.iso I downloaded earlier with UltralSO.

  13)Delete the install.esd file from the corresponding iso file, add the install.esd that you discovered, and save the file as a different name.

  14) Run the corresponding iso file as a virtual machine.

  15) As with the task condition, when I logged in to Windows, I was able to confirm that the system rebooted indefinitely after 5 seconds.

# Summary. An optional shortened abstract.
summary: let's modulate iso files to create window infinite routing through document file forensics practice


tags:
- forensic
- iso
# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

