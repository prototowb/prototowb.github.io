---
layout: post
title: "2020-02-21-100DaysOfCode-Day-1"
date: 2020-02-21 23:50:45 +0000
categories: 100-Days-of-Code challenge
---

# Day 1 of #100DaysOfCode
![Image](https://i.ytimg.com/vi/2MsN8gpT6jY/maxresdefault.jpg)
[https://pages.github.com](https://pages.github.com)
<br/>

**Todays Progress**
I finally managed to put my GitHub Pages site up (just need to implement a nav). With all the prep work, I guess I can call it Day1 of #100daysOfCode
<br/>

**Link to Project**
[here](https://prototowb.github.io)
<br/>

**Link to Tweet**
[here](https://twitter.com/prototowb/status/1230990568894930954)

```javascript
<html>
<head>
    <title>Mood Slider</title>
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
</head>
<body>
<div class="wrapper">
    <div class="container">
        <i class="material-icons" id="layout">
        view_quilt
        </i>
        <input type="range" min="0" max="4" value="2" id="slider">
    </div>
</div>
<script>
    var slider=document.getElementById("slider");
    var layout=document.getElementById("layout");
    var layoutview=["view_comfy",
    "view_module",
    "view_quilt",
    "view_compact",
    "view_stream"
    ];

    slider.oninput=function(){
        layout.innerHTML=layoutview[slider.value];
    }
</script>
</div>
</body>
</html>
```
