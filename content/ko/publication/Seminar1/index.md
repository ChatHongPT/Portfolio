---
title: "Protoy"
authors:
- 최홍석
author_notes:
- "Equal contribution"
- "Equal contribution"
date: "2024-08-21T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2024-08-21T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "BCG Lab Seminar"
publication_short: ""

abstract: |
 
  **Prototype 개념**
  
  JavaScript는 객체 지향 언어로, 다른 프로그래밍 언어와 달리 클래스 개념 대신 Prototype을 이용해 상속을 구현합니다. 모든 객체는 최상위 객체를 프로토타입으로 참조하여 상속과 비슷한 기능을 수행합니다.

  **Prototype-Pollution 정의**
  
  공격자가 JS 언어의 프로토타입 체인을 이용해 웹 서버를 공격하는 기법입니다. 객체의 프로토타입을 조작하여 예상치 못한 속성을 다른 객체에 주입하는 방식입니다.

  **Prototype-Pollution의 3가지 패턴**
  
  - **속성 설정**: 사용자 입력을 통해 객체에 새로운 속성을 추가하는 방식.
  - **객체 병합**: 재귀 병합 함수를 악용하여 프로토타입을 오염시키는 방법.
  - **객체 복사**: clone 함수 등을 사용해 객체를 복제할 때 프로토타입 오염이 발생할 수 있음.


# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: http://arxiv.org/pdf/1512.04133v1
url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---

{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).