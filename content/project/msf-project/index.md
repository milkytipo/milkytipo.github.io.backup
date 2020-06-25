---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Multi-sensor Fusion for Inspection Robot"
summary: "Introduced a loose-coupled framework that fuses IMU, SLAM, GNSS and other sensors separately, which tolerates single sensor signal lost during operation."
authors: []
tags: ["SLAM","GNSS","IMU","sensor fusion"]
categories: []
date: 2020-03-24T23:29:34+08:00

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
 - name: MSF_developed(C++)
   url: https://github.com/milkytipo/MSF_developed
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

To deploy the autonomous robot into reality,  where the robots have to cope with complicated and challenging environment, it is a tendency that fusing multi-sensor data to achieve the goal. Besides, the calibration, time synchronization and computation complexity should also be came into considered. This projects introduced a loose-coupled framework that fuses IMU, SLAM, GNSS and other sensors separately, which tolerates single sensor failure during operation.



The algorithm allowed each sensor to separately estimate their own pose, and conducted the relative-absolute relationships, for example the IMU-SLAM or SLAM-GPS. Then it would apply an error-state Kalman Filter to optimize the independent poses from SLAM and IMU, and fed back into the nominal states to acquire the genuine pose.  In this process,  the rigid constraint between the local world and vision frame should be loosed since the gravity gradually calibrate the frame into the gravity-alignment coordinate. After that, A second error-state Kalman filter was utilized to fuse the GNSS measurements to prevent state estimation drift in long-term operation.



In addition, this algorithm synchronization strategy is to interpolate single sensor measurements to the closest state in the queue.