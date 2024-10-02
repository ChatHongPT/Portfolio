---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        동네 보안 연구소🔒
      image:
        filename: welcome.jpg
      text: |
        동네 보안 연구소에 오신 걸 환영합니다! 
        해당 사이트는 최홍석의 개인 포트폴리오 사이트이며, 
        이 뿐만 아니라 다양한 보안 취약점에 대해서도 다루고 있습니다. 👨🏻‍💻
    design:
      background:
        color: '#f8f9fa'  # 밝은 회색 배경 추가
      spacing:
        padding: ['50px', '0', '50px', '0']  # 여백 조정
      css_class: hero-section  # hero 섹션에 별도의 클래스 추가

  - block: collection
    content:
      title: Latest News
      subtitle: "Check out the latest updates"
      text: "Stay up-to-date with the latest news and updates from the world of security."
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '3'  # 컬렉션을 3열로 구성하여 깔끔한 카드 형태로 표시
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: latest-news-section

  - block: markdown
    content:
      title: "Our Coders"
      subtitle: "Meet our dedicated team of developers"
      text: "We are passionate about security and innovation."
    design:
      columns: '1'
      background:
        image: 
          filename: coders.jpg
          filters:
            brightness: 0.7  # 배경 이미지의 밝기를 조금 낮춰 텍스트를 더 두드러지게
          parallax: true  # 패럴럭스 효과 추가
          position: center
          size: cover
          text_color_light: true  # 텍스트를 밝은 색상으로 변경
      spacing:
        padding: ['60px', '0', '60px', '0']  # 위아래 여백을 넉넉히 조정
      css_class: team-section

  - block: collection
    content:
      title: Latest Preprints
      subtitle: "Explore the latest research and articles"
      text: ""
      count: 5
      filters:
        folders:
          - publication
        publication_type: 'article'
    design:
      view: citation
      columns: '1'  # 단일 열로 구성하여 프리프린트 목록을 표시
      spacing:
        padding: ['30px', '0', '30px', '0']
      css_class: latest-preprints-section

  - block: markdown
    content:
      title: "Join Our Team"
      subtitle: ""
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
      spacing:
        padding: ['40px', '0', '40px', '0']
      css_class: cta-section
---
