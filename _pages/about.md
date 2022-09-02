---
permalink: /
title: "Projects"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---


MAN: Multi-Agent Networks Learning
======
We introduce a novel Deep Reinforcement Learning (DRL) algorithm called Multi-Agent Networks (MAN) Learning, to especially solve the discrete action space problems. We manually separate the action space into two smaller parts, and create one Value Neural network for each of them. Then MAN uses temporal-difference learning to train these networks synchronously, which is easier than training one networks with large action output directly. We first test MAN on a block stacking problem where we come up the basic idea of MAN, and then extend MAN for tackling 12 games with 18 action spaces of the Atari Arcade Learning environment.  
![](https://github.com/keqinw/keqinw.github.io/raw/master/images/pipeline.png "pipeline of MAN")  

MAN
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

