# Installation Guide Of Uptime_Kuma On AWS EC2 Instance.



## This Repo contains the easiest installation of Uptime Kuma the simplest and efficient monitoring System.
This tool is created by [@louislam](https://github.com/louislam), it is bassically a really nice little monitoring System for checking Your up time and few other stats.
It is very useful for web devs and Network Admins. It's Quite Something.
Well we are going to install it,but before Try its  live demo listed below
## 🥔 Live Demo

Try it!

- Tokyo Demo Server: https://demo.uptime.kuma.pet (Sponsored by [Uptime Kuma Sponsors](https://github.com/louislam/uptime-kuma#%EF%B8%8F-sponsors))
- Europe Demo Server: https://demo.uptime-kuma.karimi.dev:27000 (Provided by [@mhkarimi1383](https://github.com/mhkarimi1383))

### It is a temporary live demo, all data will be deleted after 10 minutes. Use the one that is closer to you, but I suggest that you should install and try it out for the best demo experience.


Now when you had a look so these are the features of it, but i knew that you already explored it and wanna skip to installation and you can


## ⭐ Features

* Monitoring uptime for HTTP(s) / TCP / HTTP(s) Keyword / Ping / DNS Record / Push / Steam Game Server / Docker Containers.
* Fancy, Reactive, Fast UI/UX.
* Notifications via Telegram, Discord, Gotify, Slack, Pushover, Email (SMTP), and [90+ notification services, click here for the full list](https://github.com/louislam/uptime-kuma/tree/master/src/components/notifications).
* 20 second intervals.
* [Multi Languages](https://github.com/louislam/uptime-kuma/tree/master/src/languages)
* Multiple Status Pages
* Map Status Page to Domain
* Ping Chart
* Certificate Info
* Proxy Support
* 2FA available

![uptime kuma](https://user-images.githubusercontent.com/61248381/207638893-ec43e1ed-0aed-4819-a806-9af23cf4e8d3.PNG)


# How to Install 

It's pretty new but ther are many articles,videos and installation guide but they are all self hosetd server or cloud ones are specificly on linode.
When i am trying to install it on AWS EC2 stance, i really didn't find it easy to request the web GUI page of it, as shown in above picture. Because EC2 Stance's NetworkManager doesn't allow to request any port over the internet.



## Let's Get started


###  `Setup AWS Account`


### Log in to AWS Console


### `Search for EC2 (open it)`


### Launch New Stance With Give Configuration


#### `Application OS -UBUNTU 22`

#### `Amazon Linux AMI (Default Free one)`

#### ` Instance Type- T.2 micro`

#### `Create New Key Pair -  Download it`


#### Network Settingd


##### `Allow all Traffic over the Internet` 

#### `Storage 25 GB`

### Launch It


### Login to Server Via SSH Key Pair we created earlier


## Setting Up Kuma In Machine


###  Installing ~docker
`sudo apt install docker.io`

### Installing docker-compose
`sudo apt install docker-compose -y`

### Make a Dir - MYKUMA
`mkdir mykuma`

### Make .yml file 
`sudo nano docker-compose.yml`

### copy image code - From louislam's [repository](https://github.com/louislam/uptime-kuma/blob/master/docker/docker-compose.yml) or [here](https://github.com/offseckalki/uptime_kuma/blob/main/docker-compose.yml)

### Run YML file with
`sudo docker-compose up -d`

That's it

### check if it is UP OR DOWN with
`sudo docker ps`

## Now Login to WEB GUI 
### Brows Web GUI with  publicipaddress:3001
### Now Sign Up with new user 

## Add Monitors 

![k1](https://user-images.githubusercontent.com/61248381/207663323-ecda9cf9-e9a3-48ed-b77a-2f7bf82c5b79.jpg)
![k2](https://user-images.githubusercontent.com/61248381/207662918-03c57048-0b19-4c4c-8b6e-8b6b06565773.PNG)


## Seting UP Notification
We're going to setup telegram Notification 

### Go to [BOTFATHER](https://t.me/BotFather)

### Create new bot for yourself

![k0](https://user-images.githubusercontent.com/61248381/207662975-fda5e76c-6811-4405-8d36-132e4c1ce97d.PNG)

### Copy access Token

### paste it on Web GUI form Telegram Notification setup Form 

![k3](https://user-images.githubusercontent.com/61248381/207663097-16cafe53-d727-4309-8fd6-fdba01eb3ffd.PNG)


### Click AUTOGET

### Switch Up All options 

## That's it, there you go


Whenever your website,server or any other service which you add for monitoring goes down You got a instant message on Telegram.
