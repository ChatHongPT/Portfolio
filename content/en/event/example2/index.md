---
title: Hacking Threats from LockBit 3.0 Ransomware Organizations

event: BCG LAB
event_url: https://sites.google.com/view/bcg-lab/main

location: BCG LAB
address:
  street: Chonbuk National University Engineering College Building 7, 302
  city: Jeonju City
  region: Jeonju
  postcode: '54896'
  country: Korea

summary: Analysis of security incident cases based on the latest security trend keywords
abstract: We had a practice to identify and analyze security incident cases based on the latest security trend keywords.
# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2024-04-17T13:00:00Z'
date_end: '2024-04-17T15:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2024-04-17T00:00:00Z'

authors: []
tags: ['LockBit', 'Security']

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/bzdhc5b3Bxs)'
  focal_point: Right

url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
---


LockBit 3.0 ransomware is ransomware produced by the ransomware crime organization LockBit. The hacking organization caused tremendous financial damage to companies around the world, and reemerged in early July 2022 with a version upgrade to LockBit 3.0. When LockBit 3.0 ransomware is infected, all files on the infected device are encrypted, the same as any other ransomware attack, and requires a ransom to recover data from the infected device or prevent leakage.
In addition, the recent leak of LockBit 3.0's builder source code online is expected to further increase the number of other attackers or ransomware groups that exploit LockBit 3.0 builders to carry out their own attacks. This is a serious security issue that is expected to hit more companies tremendously in the future.
LockBit3.0 ransomware distribution mail disguised as resume
The following resume email was received in a company mail in 2022. The title of the mail is 'Hu Jian', which is similar to a person's name, and the contents of the mail are ordinary contents of sending a resume to apply for a job. The mail below, forged as a resume, is an attack mail disguised as a resume to distribute LockBit 3.0 ransomware malware. The contents of the mail are about job application, but if you look closely, most of the sentences have awkward front and back contexts or misspellings. In addition, there was no separate attachment, and a file download link is inserted in the text of 'Check Portfolio'.
![LockBit] (1.png "LockBit3.0 Ransomware Distribution Mail")

When you run the resume.exe file that you downloaded from the link, the desktop background image is also changed to the image containing LocklBit Black's message. Depending on the content of the desktop, if you find and run a ransomware note named README.txt, you will see the following, and a link to the LockBit 3.0 dark website is attached with a threat that "If you don't pay for your body, I'll leak the data to the Tor dark website."
![LockBit] (2.png "PC infected with ransomware after executing History 5.exe")

LockBit 3.0 Malicious Code File Analysis Results
![LockBit] (3.png "Analyzing 'Resume 5.exe' through VirusTotal)
As a result of uploading the file to VirusTotal to analyze the "Resume 5.exe" file, 44 out of 71 anti-virus vaccines detected the "Resume 5.exe" file as a virus, and the "13.107.4.52" IP address was associated five times.
In addition, when running Resume 5.exe, a file called 96F1.tmp was stored and running somewhere, which was also detected by 56 out of 71 vaccines.
![LockBit] (2.png "96F1.tmp" Analysis with VirusTotal)
VirusTotal analysis of 96F1.temp files shows that, for 96F1.tmp files, Drop

It can be seen that a number of files corresponding to Execution Parenthood, not File, are identified.
LockBit's attack execution order is a structure in which the resume 5.exe file acts as a dropper and ransomware operates through 96F1.tmp.
In addition, 96F1.tmp also has the same IP address as the resume 5.exe file, which can be inferred that the IP address is an infected zombie server used by the attacker.
The LockBit 3.0 builder source code that is currently leaked is seriously concerned that numerous hackers will carry out such attacks on their own.
In order to prevent LockBit 3.0 ransomware attacks, it is important to register the IP address associated with LockBit 3.0 ransomware malicious code in the security system's blacklist, check if there are any doubts in the mail content when receiving e-mails such as resumes, or if there are suspicious files attached.