---
layout: page
title: Projects
description: Selected research and engineering projects.
feature_image:
tags:
---

A selection of things I've built. The first two are documented as interactive articles on this site; the rest are open source on [GitHub](https://github.com/sameerahtalafha){:target="_blank"}.

#### Multi-view 3D metrology &mdash; [interactive article]({{ site.baseurl }}/blog/from-photographs-to-a-measurable-3d-model.html)

A complete multi-view reconstruction and metrology stack &mdash; feature matching, N-view triangulation, bundle adjustment, calibrated rectification, dense stereo, and TSDF fusion &mdash; validated stage by stage against structured-light ground truth under the **official DTU evaluation protocol**. The classical, training-free pipeline reaches **0.66&nbsp;mm** overall error; plugging a modern learned multi-view depth engine (CasDiffMVS) behind the same fusion interface reaches **0.28&nbsp;mm**.

#### Cross-line part re-identification &mdash; [interactive article]({{ site.baseurl }}/blog/the-part-is-the-barcode.html)

Re-identifying physical parts across camera lines by surface appearance alone &mdash; no barcode, no tag, nothing applied. A metric embedding (IBN-ResNet50, ArcFace + supervised contrastive + triplet) with FAISS retrieval over pooled templates and an open-set novelty gate: on **502 real blocks** imaged under two lighting conditions, retrieval reaches **Rank-1 95.4% / mAP 0.968** under the enrollment protocol, while never-enrolled parts are rejected at the gate.

#### streetsight &mdash; [github](https://github.com/sameerahtalafha/streetsight){:target="_blank"}

Turns monocular street video into a live, metric 3D world: COLMAP SfM with RANSAC ground-plane scaling, replayed as a live ROS&nbsp;2 sensor world with open-vocabulary detection, ByteTrack multi-object tracking, and bilingual (English/Arabic) Qwen2.5-VL scene description &mdash; scored live against Blender-generated ground truth, fully offline on open models.

#### ur5e-box-sorter &mdash; [github](https://github.com/sameerahtalafha/ur5e-box-sorter){:target="_blank"}

Vision-guided, collision-aware pick-and-place with a UR5e in ROS&nbsp;2 Jazzy / Gazebo / MoveIt: RGB-D clustering feeds the planning scene, a verified analytic IK (&lt;1&nbsp;mm) generates exact joint-space goals, and OMPL detours around perceived obstacles &mdash; passing randomized and adversarial-obstacle missions with zero hardcoded layout.

#### tread-depth &mdash; [github](https://github.com/sameerahtalafha/tread-depth){:target="_blank"}

Metric tread-groove depth from a single uncalibrated monocular pan via visible-wall goniometry: essential-matrix + PnP camera pose and robust per-groove sinusoid fits &mdash; the method committed after empirically rejecting SfM and photometric baselines, shipped as a pip CLI with synthetic known-depth tests.
