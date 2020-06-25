---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Pseudorange Double Difference and PDR Fusion Algorithm Using Smartphone GNSS Raw Measurements"
authors: []
date: 2019-05-24T13:00:00+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2019-05-24T13:00:00+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Limited by the low-cost antenna of mobile phones and unstable crystal oscillator, the positioning accuracy of existing smartphones can only reach about 10 meters. Compared to GNSS typical shortcomings, such as weak signal, low update rate and static divergence, high update rates and independent of outside information make IMU (Inertial Measurement Unit) become an ideal fusion option. But the analysis shows that the MEMS-based IMU owes high instability and severe cumulative errors make it difficult to directly integrate with GNSS. The target of this paper is to achieve high-precision positioning by using the GNSS chip raw observation data and IMU information. Pseudorange double difference (PDD) and PDR were chosen as the fusion algorithm sub-systems. This paper analyzes the constraints of highprecision positioning of mobile phones, and then the main error sources of GNSS were eliminated by establishing a pseudorange double-difference model based on smart phones. Afterwards an error estimation model was established to induce PDR technology to correct the positioning quality in complex environments such as tunnels and tree shade, the estimator was fed back to PDR simultaneously. Ultimately, tests were carried out in various scenarios and the performance analysis of the algorithm was given. Experiments show that compared with the traditional positioning technology, PDD-PDR fusion algorithm would show obvious better positioning performance, which can achieve 5m positioning accuracy under dynamic and static alternating motion and short-time tunnel conditions."

# Summary. An optional shortened abstract.
summary: ""

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
 - name: paper
   url: "files/CSNC2019-1-EN.pdf"
   icon_pack: fas
   icon: file-pdf
 - name: slides
   url: "files/csnc_slides.pdf"
   icon_pack: fas
   icon: file-pdf


url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
