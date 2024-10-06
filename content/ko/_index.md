---
# 홈페이지 제목을 비워두어 사이트 제목을 사용
title: ""
date: 2022-10-24
type: landing

sections:

  - block: markdown
    content:
      title: ""
      subtitle: ""
      text: ""
    design:
      columns: "1"
      background:
        image:
          filename: welcome.gif
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ["20px", "0", "20px", "0"]
      css_class: fullscreen

  - block: markdown
    content:
      title: '**저는 _ _ _ _ 를 잘해요.**'
      text: |
        <br><br>**NextJS**
        **JavaScript & TypeScript**<br><br>

        ES6 자바스크립트 문법을 사용합니다.<br><br>
        TypeScript 문법에 익숙합니다.<br><br>
        TypeGuard 문법을 프로젝트에 적용한 적이 있습니다.<br><br>
    design:
      columns: "1"
      spacing:
        padding: ["20px", "0", "20px", "0"]
  
  - block: markdown
    content:
      title: '**저는 _ _ _ _ 를 잘해요.**'
      text: |
        <br><br>**ReactJS**<br><br>
        Recoil을 이용하여 전역 상태 관리를 할 수 있습니다.<br><br>
        함수형 컴포넌트 문법에 익숙합니다.<br><br>
        React hooks를 능숙하게 사용합니다.<br><br>
        
        **GIT**<br><br>

        git을 사용하여 프로젝트 관리를 합니다.<br><br>
        git-flow에 대해 압니다.<br><br>

    design:
      columns: "1"
      spacing:
        padding: ["20px", "0", "20px", "0"]

  - block: collection
    content:
      title: 🖥️ 보안 컨퍼런스
      subtitle: ""
      text: ""
      count: 5
      filters:
        author: ""
        category: ""
        exclude_featured: false
        publication_type: ""
        tag: ""
      offset: 0
      order: desc
      page_type: post
    design:
      view: community/custom_card
      columns: "1"

  - block: collection
    content:
      title: 👮🏻‍♀️ 보안 분석 자료  
      subtitle: ""
      text: ""
      count: 5
      filters:
        author: ""
        category: ""
        exclude_featured: false
        publication_type: ""
        tag: ""
      offset: 0
      order: desc
      page_type: event
    design:
      view: card
      columns: "1"
    
  - block: collection
    content:
      title: 📜 세미나 자료
      subtitle: ""
      text: ""
      count: 5
      filters:
        author: ""
        category: ""
        exclude_featured: false
        publication_type: ""
        tag: ""
      offset: 0
      order: desc
      page_type: publication
    design:
      view: community/custom_card
      columns: "1"
  
  - block: slider
    content:
      slides:
        - title: ☁️ 나에게 맞는 Cloud 학습
          content: <br><br>BCG Cloud Skills Boost로 나와 내 팀의 기술 역량을 높이세요.
          align: center
          background:
            image:
              filename: cloud.jpg
              filters:
                brightness: 0.6
            position: center
            color: '#000'
          link:
            icon: cloud
            icon_pack: fas
            text: 참여하기
            url: ../contact/

        - title: 👨🏻‍💻당신을 위한 언더그라운드 해킹그룹 HS 랩에 초대합니다.
          content: <br><br>당신의 잠재력을 HS 랩의 많은 해커들과 함께 빛낼 수 있습니다.
          align: center
          background:
            image:
              filename: security.jpg
              filters:
                brightness: 0.4
            position: center
            color: '#000'

        - title: 🔐 BCG LAB 연구실원 모집
          content: <br><br>💡 본 연구실에서 보안에 관심과 열정이 있는 연구생들을 모집합니다.
          align: center
          background:
            image:
              filename: welcome.jpg
              filters:
                brightness: 0.4
            position: center
            color: '#000'
    design:
      slide_height: '500px'
      slide_width: '110%'
      is_fullscreen: false
      loop: true
      interval: 3000
---
