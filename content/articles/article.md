---
title: Sneak Peak into how Netflix uses Neural nets.
type: page
description: Click on me to see the content.
topic: career
---

[Netflix](https://www.netflix.com/in/) uses a neural network to optimise the video content that is being streamed onto your device. To deliver the best possible video quality while you binge watch those favorite episodes, Netflix have introduced some powerful techniques into their arsenal. Every video that reaches the final customer goes through a video processing step where they have leveraged the neural networks to enhance the visuals.  
  
Video processing comprises two major steps - Video transformation & video encoding.    
- Video Transformation: Video transformation includes adjusting the video resolution to optimise picture quality under different network conditions. The traditional approach to video downscaling involves using resampling filters such as Lanczos to create multiple resolutions of the source video.    
- Video Encoding: Video encoding compresses the video to reduce the amount of data streamed to the device. This enables the video to be streamed at lower internet speeds.   
  
To improve step 1, Netflix introduced what it called "deep downscaling" which uses Neural Networks. Deep downscaler produces the best downsampled version of the content and after upscaling the mean squared error is minimal.  
  
The neural network was designed to be computationally efficient by reducing the number of layers and was applied on parts that mattered the most, and was integrated with FFmpeg and other video processes. It was made to run on CPU and GPU, and was optimised to reduce latency.  
  
🚀 Internal tests and studies concluded that deep downscaler provide significantly better visual enhancements than traditional alternatives.  

