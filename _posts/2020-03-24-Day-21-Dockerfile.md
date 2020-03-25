---
layout: post
title: "Day-21-Dockerfile"
date: 2020-03-24 21:42:45 +0000
categories: 100-Days-of-Code
---

# Day 21 of #100DaysOfCode
![Image](https://cdn.1min30.com/wp-content/uploads/2018/04/Logo-Docker.jpg)
<br/>

**Today's Progress**
Day 21 - After a long gamble on figuring out what is wrong with the FCC curriculum, the hardware from my new ISP arrived. Set it up and immediately got a hand full of issues to fix..
<br/>

There was my Pi3 failing to be reached 'from outside', the Vodafone "EasyBox" making me go nuts, then the bots i hosten on the Pi which Directories conflicted with their Git repositories.. ugh~
<br/>

so i finally decided to just pull them from Git again, somehow leaked the Bot Token in the process and had to write a new ".env" which i had slight trouble with copying it over to the Pi via scp and ftp. Oh did i mention that the Vodafone "EasyBox" messed up my WiFi and the Pi thinks it has no W-Wlan interface installed, but it has have w-lan internet connection nonetheless :'D
<br/>

So somehow i couldn't access the workdirs of the bots via ftp/scp. I was only able to place the .env in my users home directory, so i had to move it from there. Well, you know that Files starting with a "." are invisible, don't you? :) 
<br/>

after i got that, i decided i would replace the full node 'latest' package in my Docker File, ..um.. "Dockerfile", with the node:slim version. Still not quite sure about the exact differences but everything runs fine.. and is about 4-500mb smaller now :> 
<br/>
<br/>

Here it is:<br/>


```
FROM node:slim


WORKDIR /main


COPY package.json /app<br/>

RUN npm install


COPY . /main


CMD ["npm", "start"]<br/>
```


Anyone ever written a Dockerfile? Remember the contents or need to look 'em up? I'd like to have a peek :D
<br/>
**Link to Project**
[Protobwot](https://github.com/prototowb/Protobwot)
<br/>

**Link to Tweet**
[here]()
