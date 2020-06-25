---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Intelligent Robotic Navigation and Manipulation System"
summary: "Developed a docking SLAM that tracks moving objects with cm-grade docking accuracy for autonomous vehicle"
authors: []
tags: ["Docking","Semantic","Geometry Segmentation","SLAM"]
categories: []
date: 2019-06-24T23:29:34+08:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
 - name: mobile_maskrcnn
   url: https://github.com/milkytipo/mobile_maskrcnn
   icon_pack: fab
   icon: github
 - name: ORB_SLAM(developed)
   url: https://github.com/milkytipo/ORB_SLAM2
   icon_pack: fab
   icon: github

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Traditionally,  mobile robot often realized docking action with help of RFID or QR code. In autonomous factories,  to dynamically follow mobile target and then implement docking action is a pressing demand. Therefore, we aimed to develop a docking SLAM method that tracks moving objects with cm-grade docking accuracy for autonomous vehicles.



We chose Mask-RCNN build on FPN and ResNet101 to generate object masks and chose ORB_SLAM2 as back-end to realize online docking system.  In order to track the moving object, we constructed an images fusion module to combine the masks of object and depth geometry segmentation, and used omnidirectional wheels to avoid large rotation under close range.



Such a system could real-time segment out the target object from the camera images, and only extract feature points from the specific region. Without complicated mapping, the vehicle would dynamically locate and follow the target machine to dock into it.