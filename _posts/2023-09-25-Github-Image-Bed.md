---
title: "Github Image Bed"
date: 2023-09-25 20:22
toc: true
categories:
- Post
tags:
- learn
cover: /myimg/Image-Bed.jpg
---

## Background

* It is a catastrophe when trasfering markdown files from one desktop to another without encompassing all the images embeded. Therefore, an image bed is imperative and urgent to be setup. I've noticed some solutions on the internet using [PicGo](https://github.com/Molunerfinn/PicGo). Yet it is not delicate enough since it has to support various platforms. Thus, after discovering, I found Github Api is all you need to full-fill the requirement.

## Intuitions
* Image bed does one and the only thing, storing images and being accessed through internet. 
* With Github's Apis, it is extremely plain to automatically upload images.

## Github Repo Setup
* A public-reacheable repo can be easily setup.
* A Token has be to generated and granted with the following Scopes.
    * ![image_2023-09-25-20-11-38](https://raw.githubusercontent.com/ChrisVicky/image-bed/main/2023-09/image_2023-09-25-20-11-38.png)

* The following information must be granted to continue
    * `owner`: Your Github Name
    * `repo`: Your Repo Name
    * `token`: Key to Authorization

## Program and automation
* A [Program](https://github.com/ChrisVicky/image-bed-go) written in Golang is then conducted with [Github Api Wrapper](github.com/google/go-github/v55/github), which basically does one thing: *Write an image, stored locally, to github and return its url.*
* To embed the Process with my workflow -- using vim, I slightly modify the [img-paste plugin](https://github.com/ChrisVicky/img-paste.vim) to use the script.
* Illustration:
![vim-image-bed-integration](/myimg/vim-image-bed-integration.gif)
