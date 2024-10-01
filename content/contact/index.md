---
title: Contact
date: 2024-10-01

type: landing

sections:
  - block: markdown
    content:
      title: ""
      subtitle: ''
      text: |-
        <h2 style="font-size:2.5em; color:#F0E68C;">"호기심으로"</h2>
        <h1 style="font-size:3em; font-weight:bold;">개발에 몰입하는 개발자<br>유시온 입니다.</h1>
        <p style="font-size:1.2em; color:#F0E68C;">“노력은 기회를 만들고, 기회는 경험을 만들고, 경험은 지식을 만든다.”</p>
        <p style="font-size:1.1em;">라는 가치관으로 무엇이든 경험하려고 합니다.<br>꾸준한 노력 덕에 교내대회에서 수상하여 외부에서 다양한 부스 운영한 경험이 있습니다.</p>
        <p style="font-size:1.1em;">사용자 경험을 중요하게 생각합니다.<br>기준에 부합하여 학교와 외부 프로젝트에 몰두한 경험이 있습니다.</p>
    design:
      columns: '1'
      background:
        image: 
          filename: contact.jpg  # 배경 이미지 설정
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen

  - block: contact
    content:
      title: Contact
      text: |-
        <br> <span style="font-size:95%">"호기심으로"</span> <br>
      email: suk924600@naver.com
      phone: 010-2421-9246
      address:
        street: 전북대학교 공과대학 7호관 302호
        city: 전주시
        region: 전라북도
        postcode: '54896'
        country: 대한민국
        country_code: KO
      coordinates:
        latitude: '35.84601324617979'
        longitude: '127.13444961966684'
      directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      office_hours:
        - 'Monday 10:00 to 13:00'
        - 'Wednesday 09:00 to 10:00'
      appointment_url: 'https://calendly.com'
    
      autolink: true
    
      form:
        provider: netlify
        netlify:
          captcha: false
    design:
      columns: '1'

---
