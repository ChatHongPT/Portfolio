---
title: 'Slow HTTP DoS 공격에 대한 분석'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - 최홍석

# Author notes (optional)
author_notes:
  - 'BCG Lab 학부연구생'

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
 
  **<Slow HTTP DoS 공격에 대한 분석>**

  **DoS 공격**
  -공격 대상 시스템 또는 서버에 과도한 부하를 발생시켜 다른 이들이 서비스를 이용하지 못하도록 방해하는 공격 기법
 
  **DDoS공격**
  -서비스 중단을 목적으로 공격 대상에게 대용량 트래픽을 전송해 서비스의 가용량을 침해하여 다른 이용자가 서비스를 이용하지 못하도록 방해하는 공격
  대규모 커뮤니티 집단에서 하나의 웹 사이트를 새로고침 하나로 무너뜨린 사례도 있음
  -> 연속 새로고침만으로도 무차별적인 트래픽을 전송할 수 있기에 가능한 공격 기법

  **Slow HTTP DoS** 
  -공격 대상 서버에 HTTP 요청 패킷의 Header를 변조해서 동시에 많은 HTTP 연결을 유지하여 서버의 가용량을 침해하는 DoS 공격 기법
  -서버마다 요청을 처리하는 가용량이 있지만, 해당 기법은 서버에게 요청을 매우 천천히 전송하거나 Header를 변조하여 요청이 끝나도 연결을 끊지 못하도록 하는 공격기법

  **Slow HTTP DoS 종류**

  - **Slow HTTP Header DoS**: 요청 Header의 끝을 의미하는 빈 라인의 개행을 전달하지 않고, 지속적으로 불필요한 Header를 추가하여 연결 상태를 유지하는 공격기법
  - **Slow HTTP POST DoS**:  RUDY 라고 불려지는 공격 기법, 헤더 필드의 Content-Length를 비정상적으로 크게 설정한 후, 매우 작은 데이터를 천천히 웹 서버에 전송하여 연결 상태를 유지하여 웹 서버의 가용량을 침해하는 공격
  - **Slow HTTP Read DoS**: HTTP 요청을 전송한 후 Windows 크기를 아주 작게 설정하여 연결 상태를 유지하며 웹 서버의 가용량을 침해하는 공격(무한  대기 상태)

  **RUDY Attack**
 
  -Slow HTTP DoS 공격 기법 중 POST DoS에 해당
  -개발자의 보안 설정 오류나 App, 프레임워크가 최신 버전이 아닐 경우 취약점을 활용한 공격 기법 중 하나

  **[실습]**

  -bee-box IP [희생자] : 192.168.92.137

  -Kali-Linux IP [공격자] : 192.168.43.178

  **▶공격 시나리오**
  1) Kali-Linux를 활용해 bee-box Server에 Slow HTTP DoS 공격을 수행하여 bee-box Server의 가용량을 모두 차지하여 다른 사용자가 접속하지 못하게 한다.
  2) 공격 실습에서는 칼리 리눅스의 slowhttptest 도구를 활용(slowhttptest 도구 -> Slow HTTP DoS 공격 테스트 도구)
  3) 공격 실습하기 전, RUDY Attack에 사용되는 패킷에 대해 분석하기 위해 Kali-Linux에서 WireShark를 실행킨다.
  4) WireShark를 실행시킨 후, 다음과 같은 필터를 걸어준다.
  -> ip.addr == [bee-box IP] && ip.addr == [Kali-Linux IP]
  5) 칼리 리눅스에 slowhttptes 도구를 설치한다.

  **[테스트할 공격 기법 선택]**

  -H : Slowloris 공격
  -B : RUDY 공격
  -R : Apache Killer 공격
  -X : Slow Read 공격(Slow HTTP Read Dos)

  -Bee-Box Server에 RUDY DoS 공격을 수행하기 위해 다음과 같은 명령어를 사용했다.
  -> slowhttptest -B -t [임의의 문자열] -c 4000 -u http://[bee-box IP]:80

  **[공격 기본 설정]**

  -t  : 요청 시 사용할 메소드 값 (default: Slow HTTP Attack인 경우 GET / Slow HTTP Body Attack인 경우 POST)
  -c : 공격 대상에 연결할 연결 개수 설정 (default : 50)
  -u : 공격대상의 url 설정

  **[공격 분석]**

  -Content-Length가 4096으로 slowhttptest의 명령어 기본 값으로 설정된 것을 볼 수 있고, body 영역에 랜덤한 문자열이 들어감을 확인
  -첫 번째 줄에 GET이나 POST 같은 정상적인 메소드가 아닌 slowhttptest 명령어의 -t 옵션으로 지정한 값이 메소드로 들어감

  **[대응 방안]**

  -연결 Time out 설정으로 일정 시간 이상 연속된 데이터를 보내지 않는 접속자에 대해 차단

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

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

url_pdf: ''
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

