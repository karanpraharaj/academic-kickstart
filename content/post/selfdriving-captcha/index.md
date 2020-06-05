---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "You Are Building Self-Driving Cars. For Free."
subtitle: ""
summary: "We are all unwittingly cleaning the data which trains algorithms deployed in self-driving cars."
authors: ["Karan Praharaj"]
tags : ["Deep Learning", "Artificial Intelligence"]
categories : ["Computer Science", "Twitter Threads"]
date: 2020-06-05T03:03:14+05:30
lastmod: 2020-06-05T03:03:14+05:30
featured: false
draft: false
comments: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
Everytime you solve a reCaptcha image, like [this one](https://3.bp.blogspot.com/-zyPGTDdb_1I/W8gUyBlM9QI/AAAAAAAAe7M/Uj0vOL5JTRUoayUosmwswptEDIkgVT28ACLcBGAs/s400/pic.jpg), you are unwittingly cleaning the data which trains machine-learning algorithms deployed in self-driving cars. This twitter thread explains how.

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">Wonder how many people realise that they are training algorithms for self-driving cars when they solve captchas</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268613825772716032?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">When you solve a captcha image, you&#39;re now doing more than just proving that you&#39;re not a robot. You are actively teaching a (future) self-driving car to see stuff and identify it.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652639115456512?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">This is similar to teaching a baby to identify stuff by showing them the same things over and over again until they learn from their mistakes and start getting their identifications right. This feedback loop of learning-testing-evaluating-relearning is at the heart of this.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652642751954947?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">To be able to self-drive, your AI needs to learn to process, assess and then act on its surroundings. One way to &quot;learn&quot; the &quot;surroundings&quot; is to see a shitload of images of objects that it can potentially encounter in an on-road environment, and learn to classify them correctly.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652644572291072?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">Self-driving car companies develop machine learning algorithms that automatically classify these images (one eg. is classifying whether a zebra crossing is present in the field of view or not).</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652646279393280?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">These classifier algos are then fed or &quot;trained&quot; with tens of millions of pictures, until their accuracy crosses a certain minimum threshold. However, merely getting more predictions right than wrong doesn&#39;t cut it for the self-driving problem. There are literal lives at stake.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652648506494983?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">Even 80% isn&#39;t good enough. (Imagine misidentifying stuff 20% of the time while driving on road.) The pictures have to be sufficiently exhaustive of possible scenarios AND need the classifier to barely make any mistakes on them.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652650284924929?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">And so because it is crucial to stamp out almost ALL wrong predictions made by these algos, they need to be verified. This is where you - as someone who is much more reliable at identifying stuff than the algo is - come in to the picture.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652652038180864?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">These soft classified images are presented to you in the form of captcha images of streets, traffic lights, pedestrian crossings, animals, footpaths, other vehicles etc.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652653782982656?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">When your captcha-selection agrees with the classifier&#39;s prediction (&quot;annotation&quot;), the confidence in that prediction increases. When there is a mismatch, the confidence drops. If the confidence drops beyond a certain threshold, the prediction is replaced with the &quot;correct&quot; label</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652655502594050?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">This task of annotating and labeling billions of images that capture an infinite number of road-situations/-surroundings, is virtually impossible for any company with a limited workforce.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652657264246786?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">So somebody very clever came along and devised this method to trick us all into working for them without paying us a single penny. Now all your successful captchas are used to fine-tune the data that trains the brains of these cars.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652659025817601?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">(This is a very simplistic explanation of self-driving which doesn&#39;t even venture into how the actuations interact with the decision-systems. Self-driving is a much, much harder problem than this thread might make you believe.)</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652660770603011?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<center><blockquote class="twitter-tweet" data-conversation="none"  data-theme="dark"><p lang="en" dir="ltr">Next time you see an autonomous vehicle, you know that you made it what it is today.</p>&mdash; Karan (@IntrepidIndian) <a href="https://twitter.com/IntrepidIndian/status/1268652662557487108?ref_src=twsrc%5Etfw">June 4, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script></center>

<br/>

------

*You can follow me on Twitter [here](https://twitter.com/IntrepidIndian).*

