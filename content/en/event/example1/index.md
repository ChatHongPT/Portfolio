---
title: Analysis of Phishing Threats on Telegram Sites

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

Telegram is a security-focused messenger application that can be conveniently used in any device, including smartphones, PCs, and tablets. However, the number of hacking cases using Telegram messengers has been increasing rapidly in recent years, requiring users to pay attention. Hackers used traditional phishing methods to steal users' personal information through Telegram. Why is classical phishing still used today? It is because the general public thinks that Telegram is highly secure, so hackers exploited it.
![telegram] (1.png "Telegram phishing attacks and account theft flowchart")

Phishing attacks have mainly occurred in Korea to steal portal site accounts, but a number of phishing attacks targeting domestic Telegram user accounts have also been detected since early July 23. The recent Telegram phishing attack carries out a second account takeover attack on acquaintances by sending additional messages such as "account re-authentication required" and "update the latest version" to acquaintances of registered contacts after the first account is stolen. In particular, Telegram login phishing sites are difficult to distinguish, so that they cannot be judged even with the naked eye.
![telegram] (2.png "Telegram Login Phishing Site and Phishing-Induced Text")

If a user is deceived by a phishing site to enter a phone number, the hacker runs a malicious script and attempts to authenticate the login from the new device to an account intercepted by an official Telegram web server. If Telegram's second-stage authentication is disabled, the hacker only needs a phone number and authentication code to log in to the user's account. Once a hacker steals a session through Telegram web login, he or she can effectively take full control of the Telegram account, including existing conversation content and contacts.
![telegram] (3.png "Step-by-step attack method using Telegram phishing site")

2. Telegram Impersonation Phishing Site Analysis Results
As a result of a detailed analysis of the Telegram phishing site, account information necessary for Telegram web login, such as authentication keys, invitation codes, phone numbers, and tokens, is collected. Once you access the site, the country and national phone number are automatically entered based on the IP you access. It is estimated that the attacker's server has an automated phishing tool that collects a list of accounts and contacts stolen by the first attack and sends messages for the second account takeover. Currently, a simple login phishing site is being produced based on source codes published on open sources, but it is expected to evolve into a more sophisticated attack in the future, which is a session interception technique that extracts web browser information without users' knowledge.
![telegram] (4.png "malicious script that leaks account information from Telegram phishing sites")

Users should refrain from setting up secondary authentication when accessing the messenger application and accessing sites with unclear sources in order to strengthen the security of personal PCs and smartphones, as such, mobile hacking can occur regardless of Android or iPhone devices. Never access or enter user information if you receive a phishing message.