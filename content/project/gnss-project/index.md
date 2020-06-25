---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "High-accuracy GNSS Positioning on Portable Smartphone"
summary: "Developed an algorithm which achieved high-accuracy and reliable positioning of smartphones under complex environment using GNSS-IMU fusion."
authors: []
tags: ["GNSS","PDR","Smartphone"]
categories: []
date: 2017-09-24T23:29:34+08:00

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
 - name: RawMeaLogger(Android app)
   url: https://github.com/milkytipo/RawMeaLogger
   icon_pack: fab
   icon: github
 - name: PDR+RTD(matlab)
   url: https://github.com/milkytipo/PDR_coupled_GNSS
   icon_pack: fab
   icon: github
 - name: RTD(java)
   url: https://github.com/milkytipo/DDKalmanFitlerManager
   icon_pack: fab
   icon: github
 - name: paper(RTD)
   url: "files/ION.pdf"
   icon_pack: fas
   icon: file-pdf
 - name: slides(PDR/GNSS)
   url: "files/csnc_slides.pdf"
   icon_pack: fas
   icon: file-pdf


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

Google released Android Nougat (version 7.0) in 2016, which opens the possibility to use raw data to achieve high precision  solutions on low-cost smart devices. Due to the poor performance of the low-cost antenna and crystal oscillator of smartphone,  the accuracy of traditional single point positioning can only reach about 10 meters. However, IMU, the interoceptive sensor which never care about the interference outside, enable to assist GNSS to achieve robust and continuous localization.  Therefore, this project aimed to develop an algorithm which achieved high-accuracy and reliable positioning of smartphones under complex environment using GNSS-IMU fusion.



We developed an Android application to obtain the raw GNSS chips data and parsed it into generic format RINEX 3.02. During the analysis, we found that phone horrible oscillator existed intermittent 256ns drift. Then the pseudorange double-difference (PDD) was performed to eliminate the atmosphere, satellite, and phone clock error, as well as decoupled the pseudorange and velocity measurements based on the short-baseline hypothesis.



Furthermore, the joint heading estimation using Pedestrian Dead Reckoning (PDR) and GNSS Doppler was also presented, the result shows that this algorithm calibrated the PDR gait length loss and heading drift in the long-term, and maintained high smooth and accuracy in the short-term.