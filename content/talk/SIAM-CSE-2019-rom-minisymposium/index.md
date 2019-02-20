+++
title = "SIAM CSE 2019 Rom Minisymposium"
date = 2019-02-20T08:58:37-05:00  # Schedule page publish date.
draft = false

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_start = 2019-02-25T16:10:00-05:00
time_end = 2019-02-25T16:30:00-05:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Joseph Daws","Armenak Petrosyan", "Hoang Tran","Clayton Webster"]

# Abstract and optional shortened version.
abstract = "Real-world images and signals are known to be sparse in a wavelet basis. In this work, we propose a convex optimization approach, based on weighted l1-regularization, for reconstructing a signal of interest by identifying the coefficients in a sparse wavelet approximation. The vector of wavelet coefficients that form this approximation is obtained by finding the minimizer to our proposed weighted optimization problem where the weights are chosen to be the uniform norms of the wavelet basis functions. We illustrate the effectiveness of this method by solving the image inpainting and image denoising problems. The constraints of the optimization problem are either a set of subsamples in the case of the inpainting problem or a set of noisy observations in the case of the denoising problem."
abstract_short = "We consider recovering real-world images and signals by identifying their wavelet coefficients using a weighted l1 minimization problem and a small number of measurements of the signal."

# Name of event and optional event URL.
event = "SIAM CSE 2019"
event_url = "https://www.siam.org/Conferences/CM/P/PA/cse19-program-abstracts"

# Location of event.
location = "Room: 206C -- Spokane Convention Center, 334 W Spokane Falls Blvd, Spokane, WA 99201"

# Is this a selected talk? (true/false)
selected = false

# Projects (optional).
#   Associate this talk with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = ["image-inpainting"]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = ""
url_code = ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++
