---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Bluetooth Indoor Positioning System"
summary: "Aim to realize accurate Bluetooth signal arrival-of-angle (AOA) estimation, using single channel 6-antenna array."
authors: []
tags: ["Bluetooth 4.0","AOA","MUSIC"]
categories: []
date: 2018-9-24T23:29:34+08:00

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
 - name: AOA(matlab)
   url: https://github.com/milkytipo/AOA_estimation
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

Generally, only UWB (bandwidth=500M) enabled to achieve cm-grade accuracy for ratio signal positioning. However, the Bluetooth low energy 4.0 (BLE)  signal (bandwidth=2M) and subsequent BLE 5.0, hold ambition to realize cm-grade accuracy with many specific characteristics. If so, the cost of cm-grade positioning would dramatically decrease. Therefore, this project aimed to realize accurate Bluetooth signal arrival-of-angle (AOA) estimation (less than 5-degree), using single channel 6-antenna array.



The Multiple Signal Classification algorithm (MUSIC) on phase and frequency was performed to estimate angles. On frequency analysis, we found that there was a tricky phase drift problem caused by antenna switch would disturb the whole sampling result. We solved this problem by intermittent sampling with frequency compensation, and enlarging the switch time to divide the whole points into three patches which deleted points around switch time.  The multipath effect was mitigated by antenna dynamic signal polarization switch.



As a result, the algorithm achieved 5-degree accuracy in estimating the AOA of Bluetooth signal, which means cm-grade localization accuracy could be achieved with this system.