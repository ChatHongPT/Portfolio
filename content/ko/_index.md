---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:

  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: welcome.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen

  - block: markdown
    content:
      title: '**저는 _ _ _ _ 를 잘해요.**'
      text: |
        **NextJS**<br><br>
        <br><br>**JavaScript & TypeScript**<br><br>
        ES6 자바스크립트 문법을 사용합니다.<br><br>
        TypeScript 문법에 익숙합니다.<br><br>
        TypeGuard 문법을 프로젝트에 적용한 적이 있습니다.<br><br>
    design:
      columns: '1'
      spacing:
        padding: ['20px', '0', '20px', '0']
  
  - block: markdown
    content:
      title: '**저는 _ _ _ _ 를 잘해요.**'
      text: |
        <br><br>**ReactJS**<br><br>
        Recoil을 이용하여 전역 상태관리를 할 수 있습니다
        함수형 컴포넌트 문법에 익숙합니다.<br><br>
        React hooks를 능숙하게 사용합니다.<br><br><br><br>
        **GIT**<br><br>
        git을 사용하여 프로젝트 관리를 합니다.<br><br>
        git-flow에 대해 압니다.<br><br>
    design:
      columns: '1'
      spacing:
        padding: ['20px', '0', '20px', '0']

  
  - block: slider
    content:
      slides:
        - title: ☁️ 나에게 맞는 Cloud 학습
          content: BCG Cloud Skills Boost로 나와 내 팀의 기술 역량을 높이세요.
          align: center
          background:
            image:
              filename: cloud.jpg
              filters:
                brightness: 0.6
            position: center
            color: '#000'
          text: {% cta cta_link="./people/" cta_text="Meet the team →" %}

        - title: 👨🏻‍💻당신을 위한 언더그라운드 해킹그룹 HS 랩에 초대합니다.
          content: 당신의 잠재력을 HS 랩의 많은 해커들과 함께해서 빛낼 수 있습니다.
          align: center
          background:
            image:
              filename: security.jpg
              filters:
                brightness: 0.4
            position: center
            color: '#000'

        - title: 🔐 BCG LAB 연구실원 모집
          content: 💡 본 연구실에서 보안에 관심과 열정이 있는 연구생들을 모집합니다.
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

  - block: collection
    content:
      title: Latest Preprints
      text: ""
      count: 5
      filters:
        folders:
          - publication
        publication_type: 'article'
    design:
      view: citation
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '1'
---
