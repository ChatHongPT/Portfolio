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
      title: '기술스택'
      subtitle: ''
      text: |
        - ![React](/assets/media/react.svg)
        - ![Linux](/assets/media/linux.svg)
        - ![JavaScript](/assets/media/javascript.svg)
        - ![Kubernetes](/assets/media/kubernetes.svg)
        - ![MySQL](/assets/media/mysql.svg)
    design:
      columns: '1'



  - block: collection
    content:
      title: 기술스택
      subtitle: ''
      text: ''
      count: 5
      items:
        - title: React
          image: reactjs.png
          text: 리액트는 사용자 인터페이스를 구축하기 위한 자바스크립트 라이브러리입니다.
        - title: Linux
          image: linux.png
          text: 리눅스는 오픈소스 운영체제입니다.
        - title: JavaScript
          image: javascript.png
          text: 자바스크립트는 웹 개발에 사용되는 프로그래밍 언어입니다.
        - title: Kubernetes
          image: kubernetes.png
          text: 쿠버네티스는 컨테이너화된 애플리케이션을 자동으로 배포, 관리합니다.
        - title: MySQL
          image: mysql.png
          text: MySQL은 관계형 데이터베이스 관리 시스템입니다.
    design:
      view: card
      columns: '1'

  
  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: coders.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen

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
