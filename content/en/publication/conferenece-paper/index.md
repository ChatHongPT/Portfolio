---
title: 'Analysis of Slow HTTP DoS Attacks'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - CHOI HONG SEOK

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
  **<Analyzing Slow HTTP DoS Attacks>**

  **DoS attacks**
  -An attack technique that creates excessive load on the target system or server and prevents others from using the service

  **DDoS attack**
  -Attacks that send large amounts of traffic to the target to disrupt the service and infringe on the availability of the service, preventing other users from using the service
  Large community groups have broken down one website with one refresh
  -> Attack techniques that allow indiscriminate traffic to be transmitted with only consecutive refreshes

  **Slow HTTP DoS**
  -DoS attack technique that modulates the header of the HTTP request packet on the attack target server to maintain many HTTP connections at the same time, thereby infringing on the server's availability
  -Each server has the capacity to process requests, but this technique sends requests to servers very slowly or modulates the header to prevent them from disconnecting when the request ends

  **Slow HTTP DoS Types**

  - **Slow HTTP Header DoS**: Attack technique to maintain connection by continuously adding unnecessary headers without forwarding the opening of an empty line, which means the end of the request header
  - **Slow HTTP POST DoS**: An attack technique called RUDY, which sets the content-length of the header field to abnormally large, and then slowly transfers very small data to the web server to remain connected, violating the availability of the web server
  - **Slow HTTP Read DoS**: After sending HTTP requests, set the Windows size very small to stay connected and attack the availability of web servers (infinite standby)

  **RUDY Attack**

  -Corresponds to POST DoS among Slow HTTP DoS attack techniques
  -One of the attack techniques that exploit vulnerabilities if the developer's security settings errors, apps, and framework are not up to date

  **Practice**

  -Bee-box IP [victim]: 192.168.92.137

  -Kali-Linux IP [attacker]: 192.168.43.178

  **▶ Attack Scenario**
  1) Kali-Linux is used to perform a slow HTTP DoS attack on the beep-box server to take up all the available capacity of the beep-box server, preventing other users from accessing it.
  2) In attack practice, Kali Linux's slowhttptest tool is utilized (slowhttptest tool -> Slow HTTP DoS attack test tool)
  3) Before practicing the attack, we run WireShark on Kali-Linux to analyze the packets used in the RUDY Attack.
  4) After running WireShark, apply the following filter.
  -> ip.addr == [bee-box IP] && ip.addr == [Kali-Linux IP]
  5) Install the slow httptes tool on Kali Linux.

  **[Choose the attack technique to test]**

  -H: Slowloris attack
  -B: RUDY attack
  -R : Apache Killer 공격
  -X : Slow Read 공격(Slow HTTP Read Dos)

  -The following commands were used to perform a RUDY DoS attack on the Bee-Box Server.
  -> slowhttptest -B-t [any string] -c4000 -uhttp://[bee-box IP]:80

  **[Attack preference]**

  -t : Method value to use on request (default: GET / POST for Slow HTTP Body Attack)
  -c : Set the number of connections to be connected to the attack target (default : 50)
  -u : setting the url of the attack target

  **[Analyzing the attack]**

  -You can see that the content-length is set to 4096 as the command default value of slowhttptest, and you can see that the body area contains a random string
  -The first line contains a value specified by the -t option of the slowhttptest command rather than a normal method such as GET or POST

  **[Response plan]**

  -Connection Time out setting blocks connectors who do not send consecutive data for a certain period of time or longer

# Summary. An optional shortened abstract.
summary: DoS attack technique that modulates the header of the HTTP request packet on the attack target server to maintain many HTTP connections at the same time, thereby infringing on the server's availability

tags:
- DoS
- DDoS
- Network Security

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://github.com/ChatHongPT/JBNU_HONGSEOK.github.io/blob/main/content/ko/publication/conferenece-paper/conference-paper.pdf'
url_code: 'https://github.com/sahilchaddha/rudyjs'
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

