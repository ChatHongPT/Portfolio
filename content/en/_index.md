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
          filename: welcome.png
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
      title: '**I _ _ _ _ good at this.**'
      text: |
        <br><br>**NextJS**
        **JavaScript & TypeScript**<br><br>

        Use ES6 JavaScript grammar.<br>
        I am familiar with TypeScript grammar.<br>
        TypeGuard grammar has been applied to projects.<br><br>
    design:
      columns: '1'
      spacing:
        padding: ['20px', '0', '20px', '0']
  
  - block: markdown
    content:
      title: '**I_ _ _ _ good at this.**'
      text: |
        <br><br>**ReactJS**<br><br>
        Recoil allows for global health management <br><br>
        You are familiar with functional component grammar.<br>
        Use Reacthooks skillfully.<br>
        
        **GIT**<br><br>

        Use git to manage projects.<br><br>
        I know about git-flow.<br>    

    design:
      columns: '1'
      spacing:
        padding: ['20px', '0', '20px', '0']

  
  - block: slider
    content:
      slides:
        - title: ☁️ Learn the right cloud for me
          content: <br><br>Boost my team's technical capabilities with BCG Cloud Skills Boost.
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
            text: Join Us
            url: ../contact/

        - title: 👨🏻‍💻I invite you to the underground hacking group HS Lab for you.
          content: <br><br>You can shine your potential with a lot of hackers in HS Lab.
          align: center
          background:
            image:
              filename: security.jpg
              filters:
                brightness: 0.4
            position: center
            color: '#000'

        - title: 🔐 Recruitment of BCGLAB Laboratories
          content: <br><br>💡 We are recruiting researchers who are interested in and passionate about security in this laboratory.
          align: center
          background:
            image:
              filename: welcome.png
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
