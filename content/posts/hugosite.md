---
title: "Some things to consider when making a HUGO site"
date: 2022-11-13T06:00:23+06:00
hero: /images/posts/hugohero.jpg
description: Things I would've been helpful, had I known them when making my HUGO site.
theme: Toha
menu:
  sidebar:
    name: Some things to consider when making a HUGO site
    identifier: hugosite
    weight: 500
---

### So, I made a HUGO site.

Yay! While it took me longer than expected to finish, I still made a website faster than if I were to use HTML and CSS. HUGO's framework is relatively easy to use, and I would definitely recommend it, as you get both presentation and functionality in a short amount of time.

I've compiled a list of some of the most annoying errors that I ran into so you don't have to suffer through them!

### 1. nilPointer errors when setting background

Apparently, HUGO has a specific file structure that it likes, so make sure to copy the folder structures exactly from the theme example. For example, even though "assets" only contains an "images" folder, an error is raised when there is no "assets" folder present because HUGO cannot find the file.

HUGO, unfortunately, hates flexibility :(

### 2. Netlify fails to deploy site, Exit Status 128

When I was trying to figure out how to set the background, I changed the default-background.jpg in themes/toha/assets/images to a different image to test if the website would change. I also accidentally committed those changes, which I didn't realize until I started to try to deploy the site. After like an hour of trying to figure out what the error was, I finally remembered that I had changed the original themes package. Netlify doesn't like it when that happens, so make sure to NOT TOUCH THE THEMES FOLDER. I reversed my commits and I was able to deploy the site!
