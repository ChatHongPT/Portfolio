---
title: 'ChatGPT의 보안 위협 분석'

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
 
  1) ChatGPT가 생성하는 결과물을 사이버 공격에 이용
  ChatGPT를 통해 대량의 피싱 메일 작성을 손쉽게 할 수 있고, 섬세한 수정이 가능하며 피싱 메일이 전보다 더 정교해지며, 해외 공격자들은 언어적 한계를 해소하며 자연스러운 피싱 메일을 작성할 수 있게 되었다. 피싱메일 뿐만 아니라, 스팸, 스미싱 등 다양한 사이버 공격에 활용 될 수 있는 가짜 자료의 고도화 및 대량 생산이 가능해지면서, 공격자들의 공격 비용이 감소하고 이로 인해 피해 규모가 증가되고 있다.
 
  2) ChatGPT가 생성한 악성코드
  ChatGPT의 코드 생성 기능을 악용하여 해컹릐 해킹도구 제작에 도움을 줄 수 있고, 개발
  지식이 없는 일반인 조차도 ChatGPT를 통해 보다 쉽게 해킹도구를 제작할 수 있다. 생성형 AI는 해킹 도구 개발의 시간적 비용을 감소시키고, 무분별한 사이버 범죄 발생 및 일반 범죄의 사이버 범죄 가능성이 존재한다.
  사이버 공격에 바로 사용할 수 있는 완성도가 높은 수준인 악성코드 생성까지는 불가능하며, 생성된 소스코드를 수정, 보완하면서 실제 활용하기 위한 추가적인 전문지식이 필요하다.
  
  3) ChatGPT를 활용한 악성코드 제작 테스트
  1. 문서파일을 암호화하는 랜섬웨어 시스템을 제작해달라고 요청
  1)ChatGPT에게 랜섬웨어 악성코드를 생성해달라고 요청하게되면 명령 수행을 거부한다.
   
  2) 랜섬웨어의 일부 기능 생성을 우회적으로 요청했을 경우 명령을 수행한다.
  2. 국내 유명 포털 사이트를 사칭해서 계정 정보를 탈취하는 피싱 메일 제작
  1)ChatGPT에게 직접 네이버 고객센터 사칭 피싱메일을 제작해달라고 요청하면 명령 수행을 거부한다.
  2) 피싱메일 키워드를 제거하고 우회적으로 메일 작성 요청시 명령을 수행한다.
 
  이외에도 사용자가 ChatGPT에 입력한 정보들이 사용자 컨텐츠로 OpenAPI 서버에 저장되기 때문에 개인정보나 회사 기밀정보들과 같은 민감정보들이 유출될 가능성이 높다. 
  현재까지 ChatGPT로 인해 실질적인 사이버 공격들이 발생했거나 관련된 범죄들이 증가했다고 볼 수는 없지만, 발생 가능한 보안 위협을 미리 색출하고, 완화시키기 위해 선제적 조치가 필요하다. ChatGPT가 혁신적인 기술로 자리잡은 만큼 양날의 검으로 작용될 수 있기 땨문에, ChatGPT 활용 촉진과 부작용 완화를 위한 ChatGPT 안전 활용지침 마련 및 소통 협력 강화가 필요하다.
  # Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- LLM
- Security

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

