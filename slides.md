---
# You can also start simply with 'default'
theme: academic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Advanced Algorithmic Methods for Next-Generation Computational Displays
favicon: /complightlab.png
titleTemplate: '%s - Computational Light Laboratory'
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-left
# https://sli.dev/features/drawing
drawings:
  persist: false
colorSchema: dark
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: fade-out
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# take snapshot for each slide in the overview
overviewSnapshots: true
coverDate:
fonts:
  local: Montserrat, Roboto Mono, Roboto Slab
---

<div class="abs-br left-50px top-35px" style="max-width: 540px;">
<span style="font-size: 2.25em">
<b>Advancing Algorithmic Methods for Next-Generation Computational Displays</b></span>
</div>

<div class="abs-br left-50px top-315px" style="width:450px">
<span style="font-size:1.1em">
<b>Yicheng Zhan</b>
</span>
</div>

<div class="abs-br left-50px top-345px" style="width:260px">
<span style="font-size:1.1em;">
University College London
</span>
</div>

<div class="abs-br left-50px top-430px">
<img src="/complight.png" style="max-height: 80px; max-width: 80px;">
</div>

<div class="abs-br left-130px top-435px" style="width:200px">
<a href="https://complightlab.com">
<span style="font-size:1.2em;">
Computational Light Laboratory
</span>
</a>
</div>


<div class="absolute right-275px bottom-20px">
<a href="">
<img src="/teaser.png" style="max-height: 200px; max-width: 200px;">
</a>
</div>

<div class="absolute right-25px bottom-20px">
<a href="">
<img src="/autocolor.png" style="max-height: 200px; max-width: 200px;">
</a>
</div>


<div class="abs-br right-70px top-45px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/focal_stack_3D_side.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>

<div class="abs-br right-180px top-125px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/curve_arrow.png" style="max-height: 100px; max-width: 100px;">
  </div>
</div>

<div class="abs-br right-180px top-200px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/hologram_side.png" style="max-height: 130px; max-width: 130px;">
  </div>
</div>

<!--
Hello, everyone. 
Thank you for being here today. 
My name is YICHENG ZHAN and I am a PhD student in UCL. 
Today I'm excited to share our group`s work in siggraph asia 2024.
The title of our project is Focal Surface Holographic Light Transport using Learned Spatially Adaptive Convolutions
-->

---
transition: fade-out
layout: two-cols
---

<!-- 2D -->
# AutoColor

<div class="left-column">

<!-- 2D -->
<div v-click.hide="0">
<span style="color: #3cff19">2D Multi-color Optimization:</span>

$$
\begin{aligned}
\hat{u_t}, \hat{l}_{(p,t)} \leftarrow \argmin_{u_t, l_{(p,t)}} \mathcal{L}\left( \sum_{p=1}^3 \sum_{t=1}^3 |l_{(p,t)} e^{i \lambda_p u_t} * h_p |^2 , sI_p \right),
\end{aligned}
$$
</div>
<!-- <div v-click="[1,2]"> -->
<div v-click="0">
<span style="color: #3cff19" class="abs-br left-56px top-92px">2D Multi-color Optimization:</span>
<div class="abs-br left--452px top-123px">
$$
\begin{aligned}
\hat{u_t}, \textcolor{3cff19} {\hat{l}_{(p,t)}} \leftarrow \argmin_{u_t, \textcolor{3cff19} {l_{(p,t)}}} \mathcal{L}\left( \sum_{p=1}^3 \textcolor{fbff00}{\sum_{t=1}^3} |\textcolor{3cff19} {l_{(p,t)}} e^{i \lambda_p u_t} * h_p |^2, sI_p \right),
\end{aligned}
$$
</div>

</div>


</div>

::right::
<!-- Visual Artifact -->
<div v-click="0">

<div  class="abs-br right-183px top-48px" style="z-index: 2;">
<span style="background-color: #ff1212; color: black; padding: 2px 5px;">
<b>Visual Artifacts</b>
</span>
</div>

<div class="abs-br right-130px top-74px" style="z-index: 1;">
<div class="abs-br right-230px top-95px">
<span style="color: #ff1212">→</span>
</div>
  <div class="relative inline-block">
      <img src="/projects/AutoColor/Conventional_flower.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>

<!-- Brighter without Artifacts -->
<div v-click="0">
<div  class="abs-br right-86px top-288px" style="z-index: 2;">
<span style="background-color: #3cff19; color: black; padding: 2px 5px;">
<b>Brighter without Artifacts</b>
</span>
</div>

<div class="abs-br right-130px top-315px">
<div class="abs-br right-230px top-95px">
<span style="color: #3cff19">→</span>
</div>
  <div class="relative inline-block">
      <img src="/projects/AutoColor/Multicolor_flower.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>

<arrow v-click="0" x1="340" y1="240" x2="315" y2="204" color="#3cff19" width="2" arrowSize="1" /> 

<div v-click="0"  class="absolute left-360px top-235px text-left" style="max-height: 300px; max-width: 300px; color: #3cff19">
  <div class="relative inline-block">
    initialized by NN
  </div>
</div>

<div class="absolute right-490px top-340px text-left" style="max-height: 420px; max-width: 420px;">
  <div class="relative inline-block">
    optimization steps decreased from <span style="color: #ff1212;">> 1000</span> to <span style="color: #3cff19;">70</span> iteration steps without no image quality loss.
  </div>
</div>


<p class="citation" style="font-size: 7px; position: absolute; right: 256px; bottom: -10px; z-index: 10;">
  (1) "<a rel="noopener noreferrer" href="https://arxiv.org/abs/2305.01611" target="_blank">
  Zhan, Y., Kavaklı, K., Urey, H., Sun, Q., & Akşit, K. AutoColor: Learned Light Power Control for Multi-Color Holograms.
  </a>" <i>SPIE AR|VR|MR 2024</i>
</p>

<style>
.left-column {
  width: 70%;
  padding-right: 1rem;
}
.slidev-layout {
  display: flex;
}
</style>

<!--
The problem we faced in this project was the need for real-time generation of multi-color holograms. Compared with the traditional single color hologram, Multicolor hologram is an emerging hologram type.
Single-color holograms use a time-sequential approach. 
On the other hand, Multi-color holograms simultaneously use multiple color primaries, modulating all colors at once. which offers Improved brightness levels, and enhanced color reproduction.

Naively, when we pile up multiple colour primaries in the traditional 2D hologram it will create a visual artifacts.
You can also boost the brightness level by using more power of the laser but it may hurt your eyes.
In comparison. Multicolour hologram does not have such a visual artifacts and in fact it achieves brighter scene with lesser laser power which protects your eyes.

However optimising 3×3 equals to 9 extra variables requires precise control over multiple light sources and time consuming. 

This is where my research on autocolor goes in. 
Instead of using randomly initialised laser power as the starting point of optimisation we use NN predicted laser power to replace it.
This allows for much faster generation of high-quality, multi-color holograms.
To train such a network we created the first 3-D multicolour hologram dataet using large language model, stable diffusion and death estimation network.
-->



---
transition: fade-out
---

<div style="font-size: 37px;  max-height: 950px; max-width: 1250px;">
Conventional Light Transport
</div>

<div class="abs-br left-80px top-155px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/depth_plane_transparent.png" style="max-height: 200px; max-width: 200px;">
  </div>
  <div class="abs-br left--10px top-235px">Depth Plane</div>
</div>


<arrow  style="z-index: 2;" x1="250" y1="260" x2="300" y2="260" width="1" arrowSize="1" />

<div  class="abs-br left-320px top-175px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/focal_stack_side.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>

<div class="abs-br right-366px top-129px" style="z-index: 2;">
<span style="background-color: #ff1212; color: black; padding: 2px 5px;">
<b>Individual Propagation Per Plane</b>
</span>
</div>

<div class="abs-br left-320px top-195px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/arrow_n_steps.png" style="max-height: 220px; max-width: 220px;">
  </div>
</div>

<div class="abs-br left-280px top-355px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/hologram_side.png" style="max-height: 100px; max-width: 100px;">
  </div>
</div>

<arrow style="z-index: 2;" x1="510" y1="260" x2="560" y2="260" width="1" arrowSize="1" />

<div class="abs-br right-250px top-175px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/depth_plane_side.png" style="max-height: 200px; max-width: 200px;">
  </div>
  <div class="abs-br left--10px top-215px">Reconstruction</div>
</div>

<arrow  style="z-index: 2;" x1="750" y1="260" x2="800" y2="260" width="1" arrowSize="1" />

<div  class="abs-br right-70px top-195px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/hardware.png" style="max-height: 180px; max-width: 180px;">
  </div>
  <div class="abs-br left--10px top-195px">Holographic Display</div>
</div>


<p class="citation" style="font-size: 10px; position: absolute; right: 216px; bottom: 40px; z-index: 10;">
  (1) "<a rel="noopener noreferrer" href="https://opg.optica.org/oe/fulltext.cfm?uri=oe-17-22-19662&id=186848" target="_blank">
  Kyoji Matsushima and Tomoyoshi Shimobaba. Band-Limited Angular Spectrum Method
  </a>" <i>Optics Express 2009</i>
</p>

<p class="citation" style="font-size: 10px; position: absolute; right: 266px; bottom: 20px; z-index: 10;">
  (2) "<a rel="noopener noreferrer" href="https://opg.optica.org/oe/fulltext.cfm?uri=oe-17-22-19662&id=186848" target="_blank">
  J. W. Goodman. Angular Spectrum Method
  </a>" <i>Introduction to Fourier Optics 2005</i>
</p>

<p class="citation" style="font-size: 10px; position: absolute; right: 236px; bottom: 0px; z-index: 10;">
  (3) "<a rel="noopener noreferrer" href="https://opg.optica.org/ol/abstract.cfm?uri=ol-45-6-1543" target="_blank">
  Zhang, W. and Zhang, H. and Jin, G. Band-extended Angular Spectrum Method
  </a>" <i>Optics Letters 2020</i>
</p>

<!--
in the second project, we are addressing the simulation of light transport in holography, 
Conventionally, we propagate a given Hologram to multiple different depth planes step by step 
to generate the reconstructions of it. This is typically how things are calculated in holographic display, 

There are many existing works in the literature that help to improve the accuracy of the propagation simulation.
-->

---
transition: fade-out
---

<div style="font-size: 37px;  max-height: 950px; max-width: 1250px;">
Focal Surface Light Transport 
</div>

<div class="abs-br left-40px top-155px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/depth_plane_transparent.png" style="max-height: 200px; max-width: 200px;">
  </div>
  <div class="abs-br left--10px top-235px">Depth Plane</div>
</div>


<arrow  style="z-index: 2;" x1="210" y1="260" x2="260" y2="260" width="1" arrowSize="1" />

<div class="abs-br left-270px top-175px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/focal_stack_3D_side_grey.png" style="max-height: 170px; max-width: 170px;">
  </div>
   <div class="abs-br left-10px top-215px">Focal Surface</div>
</div>

<arrow  style="z-index: 2;" x1="440" y1="260" x2="490" y2="260" width="1" arrowSize="1" />

<div  class="abs-br right-300px top-195px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/focal_stack_3D_side.png" style="max-height: 170px; max-width: 170px;">
  </div>
</div>

<div  class="abs-br right-410px top-295px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/curve_arrow.png" style="max-height: 70px; max-width: 70px;">
  </div>
</div>

<div class="abs-br right-400px top-345px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/hologram_side.png" style="max-height: 100px; max-width: 100px;">
  </div>
</div>


<div class="abs-br right-326px top-129px" style="z-index: 2;">
<span style="background-color: #3cff19; color: black; padding: 2px 5px;">
<b>Multi-planes Propagation In One Step</b>
</span>
</div>

<arrow style="z-index: 2;" x1="680" y1="260" x2="730" y2="260" width="1" arrowSize="1" />

<div  class="abs-br right-80px top-175px">
  <div class="relative inline-block">
      <img src="/projects/Focal_Stack/depth_plane_side.png" style="max-height: 200px; max-width: 200px;">
  </div>
  <div class="abs-br left--10px top-215px">Reconstruction</div>
</div>



<p class="citation" style="font-size: 7px; position: absolute; right: 166px; bottom: -10px; z-index: 10;">
  (2) "<a rel="noopener noreferrer" href="https://kaanaksit.com/assets/pdf/ZhengEtAl_SigAsia2024_Focal_surface_holographic_light_transport_using_learned_spatially_adaptive_convolutions.pdf" target="_blank">
  Zheng, C., Zhan, Y., Shi, L., Cakmakci, O., & Akşit, K. Focal Surface Holographic Light Transport using Learned Spatially Adaptive Convolutions.
  </a>" <i>SIGGRAPH ASIA 2024 Tech Comm</i>
</p>


<!--
We propose focal surface light transport,
instead of having individual depth planes,
we first generate a focal surface based on the target depth planes and then,
we train a neural network that takes focal surface and the hologram as the input to generate the final reconstructions all in once.

So in this case, we can achieve simulating light propagation in multiple planes using only 1 step.
-->

---
transition: fade-out
---

# Result (Simulation)

<script setup>
import { ref } from 'vue'

const playbackRate = ref(0.7)
</script>


<div class="absolute right-45px top-125px text-center">
  <div style="max-height: 900px; max-width: 900px;">
    <SlidevVideo  autoplay autoreset :playbackRate="playbackRate" loop>
      <source src="/projects/Focal_Stack/changing_depth.mov" type="video/mp4" />
    </SlidevVideo>
  </div>
</div>
<div class="absolute right-465px top-85px text-center" style="background-color: #3cff19; max-height: 300px; max-width: 330px; padding: 2px 5px; z-index: 4;">
  <div class="relative inline-block">
    <span style="color: black; font-size:1.2em"><b>Ours</b></span><br>
  </div>
</div>
  <div class="absolute right-165px top-85px text-center" style="background-color: #ff1212; max-height: 300px; max-width: 330px; padding: 2px 5px; z-index: 4;">
  <div class="relative inline-block">
    <span style="color: black; font-size:1.2em"><b>ASM</b></span><br>
  </div>
</div>



<div  class="absolute left-85px bottom-25px" style="width: 80%; z-index: 10;">
  <div class="flex justify-between text-xs mb-1">
    <span>Slow (0.5x)</span>
    <span>Normal (1x)</span>
    <span>Fast (2x)</span>
  </div>
  <input 
    type="range" 
    v-model="playbackRate" 
    min="0.5" 
    max="2" 
    step="0.01" 
    class="slider"
    style="width: 100%;"
  >
</div>


<style>
.slider {
  -webkit-appearance: none;
  width: 100%;
  height: 10px;
  border-radius: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: .2s;
  transition: opacity .2s;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: #3cff19;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: #3cff19;
  cursor: pointer;
}
</style>

<p class="citation" style="font-size: 7px; position: absolute; right: 166px; bottom: -10px; z-index: 10;">
  (2) "<a rel="noopener noreferrer" href="https://kaanaksit.com/assets/pdf/ZhengEtAl_SigAsia2024_Focal_surface_holographic_light_transport_using_learned_spatially_adaptive_convolutions.pdf" target="_blank">
  Zheng, C., Zhan, Y., Shi, L., Cakmakci, O., & Akşit, K. Focal Surface Holographic Light Transport using Learned Spatially Adaptive Convolutions.
  </a>" <i>SIGGRAPH ASIA 2024 Tech Comm</i>
</p>

<!--
Here, we present a close-up reconstruction comparison 
between our method and the ASM method under varying depth planes. 
Notably, our approach closely replicates the defocus and focus effects similar to the ASM method,  
while achieving this series of propagations in one single forward pass.

new slide after, which contains new rendering result
focal surface version
-->

---
transition: fade-out
---

<div class="absolute left-90px top-15px text-left" >
<span style="font-size:2em">Configurable Learned Holography</span>
</div>


<div class="absolute left-90px top-65px inset-0 bg-white" style="z-index: 0; max-height: 400px; max-width: 800px;">
  <!-- White background container -->
</div>

<div class="absolute left-90px top-65px text-left" style="background-color: #ff1212; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Conventional Model </b> </span>
  </div>
</div>


<div v-click.hide = "1">
<span class="absolute left-390px top-160px " style="color: black; z-index: 2;">→</span>
<div class="absolute left-420px top-130px text-center" style="background-color: rgb(0, 0, 0, 0.25); max-height: 300px; max-width: 120px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:0.8em"><b>Jasper JD7714</b>
     4K resolution
     3.74μm</span>
  </div>
</div>
<span class="absolute left-390px top-260px " style="color: black; z-index: 2;">→</span>
<div class="absolute left-420px top-235px text-center" style="background-color: rgb(0, 0, 0, 0.25); max-height: 300px; max-width: 120px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:0.8em"><b>Holoeye Pluto</b>
     HD resolution
     8.0μm</span>
  </div>
</div>
</div>


<div v-click = "0">
<div class="abs-br left-166px top-118px" style="z-index: 1;">
<div class="abs-br left-150px top-5px">
  <div class="relative inline-block" >
      <img src="/projects/Configurable_holo/demo/SLMs.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>
</div>

<div v-click = "0">
<div class="abs-br left--30px top-105px" style="z-index: 1;">
<div class="abs-br left-150px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/red_NN.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>
</div>

<div v-click = "1">

<div class="absolute left-510px top-65px text-left" style="background-color: #ff1212; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Single Color Hologram Only </b> </span>
  </div>
</div>

<div class="abs-br right-60px top-105px" style="z-index: 1;">
<div class="abs-br right-50px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/results_single.png" style="max-height: 450px; max-width: 450px;">
  </div>
</div>
</div>
</div>

<div v-click = "1">
<div class="abs-br left-83px top-191px" style="z-index: 2;">
<div class="abs-br left-150px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/red_NN2.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>
</div>


<div v-click = "1">
<div class="abs-br left-200px top-175px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>


<div v-click = "1">
<div class="abs-br left-200px top-250px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>


<div v-click = "1">
<div class="abs-br left-200px top-325px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>

<div v-click = "1">
<div class="absolute left-360px top-435px text-left" style="background-color: #ff1212; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>One model per configuration </b> </span>
  </div>
</div>
</div>


<div v-click = "1">
<div class="absolute left-90px top-375px text-left" style="background-color: #ff1212; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>< 10 FPS @ full HD</b> </span>
  </div>
</div>
</div>

<div v-click = "1">
<div class="absolute left-90px top-415px text-left" style="background-color: #ff1212; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Requires Depth as input</b> </span>
  </div>
</div>
</div>
<p class="citation" style="font-size: 7px; position: absolute; right: 316px; bottom: -10px; z-index: 10;">
  (3) "<a rel="noopener noreferrer" href="https://arxiv.org/abs/2405.01558" target="_blank">
  Zhan, Y., Shi, L., Matusik, W., Sun, Q., & Akşit, K. Configurable Learned Holography.
  </a>" <i>arXiv e-prints</i>
</p>

<!--
In conventional CGH model say we have two different holographic display one and two they have different settings of course.
if I want to train a network that can adapt to display one, no problem, they usually take RGB-D as input and once the model is trained the network can give you single colour hologram 
but if you want to let it adapt to display 2,  the current model can not do that, you have to train another model for display two and then that’s also true for display 3 and 4 
the more displays you have, the more models you need to trainand. these networks will give you holograms individually so one model can only adapt to one configuration.

the state of art CGH network supports smaller than 10 FPS for full HD resolution. 
They’re slow and then they require that depth as the input.
-->

---
transition: fade-out

---


<div class="absolute left-90px top-65px inset-0 bg-white" style="z-index: 0; max-height: 400px; max-width: 800px;">
  <!-- White background container -->
</div>

<div class="absolute left-90px top-65px text-left" style="background-color: #3cff19; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Configurable Learned Holography </b> </span>
  </div>
</div>


<div v-click.hide = "0">
<span class="absolute left-390px top-160px " style="color: black; z-index: 2;">→</span>
<div class="absolute left-420px top-130px text-center" style="background-color: rgb(0, 0, 0, 0.25); max-height: 300px; max-width: 120px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:0.8em"><b>Jasper JD7714</b>
     4K resolution
     3.74μm</span>
  </div>
</div>
<span class="absolute left-390px top-260px " style="color: black; z-index: 2;">→</span>
<div class="absolute left-420px top-235px text-center" style="background-color: rgb(0, 0, 0, 0.25); max-height: 300px; max-width: 120px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:0.8em"><b>Holoeye Pluto</b>
     HD resolution
     8.0μm</span>
  </div>
</div>
</div>


<div v-click = "0">
<div class="abs-br left-166px top-118px" style="z-index: 1;">
<div class="abs-br left-150px top-5px">
  <div class="relative inline-block" >
      <img src="/projects/Configurable_holo/demo/SLMs.png" style="max-height: 200px; max-width: 200px;">
  </div>
</div>
</div>
</div>

<div v-click = "0">
<div class="abs-br left--30px top-105px" style="z-index: 1;">
<div class="abs-br left-150px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/green_NN.png" style="max-height: 280px; max-width: 280px;">
  </div>
</div>
</div>
</div>

<div v-click = "0">

<div class="absolute left-510px top-65px text-left" style="background-color: #3cff19; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Single&Multi-color Hologram</b> </span>
  </div>
</div>

<div class="abs-br right-60px top-105px" style="z-index: 1;">
<div class="abs-br right-50px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/results_ours.png" style="max-height: 450px; max-width: 450px;">
  </div>
</div>
</div>
</div>



<div v-click = "0">
<div class="abs-br left-200px top-180px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>


<div v-click = "0">
<div class="abs-br left-200px top-265px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>


<div v-click = "0">
<div class="abs-br left-200px top-333px" style="z-index: 3;">
<div class="abs-br left-200px top-5px">
  <div class="relative inline-block">
      <img src="/projects/Configurable_holo/demo/arrow.png" style="max-height: 50px; max-width: 50px;">
  </div>
</div>
</div>
</div>

<div v-click = "0">
<div class="absolute left-360px top-435px text-left" style="background-color: #3cff19; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>Multiple optical configurations </b> </span>
  </div>
</div>
</div>

<div v-click = "0">
<div class="absolute left-90px top-375px text-left" style="background-color: #3cff19; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>25 FPS @ full HD (fp32)</b> </span>
  </div>
</div>
</div>

<div v-click = "0">
<div class="absolute left-90px top-415px text-left" style="background-color: #3cff19; max-height: 300px; max-width: 500px; padding: 2px 5px; z-index: 2;">
  <div class="relative inline-block">
     <span style="color: black; font-size:1em"><b>RGB-only image as input</b> </span>
  </div>
</div>
</div>

<p class="citation" style="font-size: 7px; position: absolute; right: 316px; bottom: -10px; z-index: 10;">
  (3) "<a rel="noopener noreferrer" href="https://arxiv.org/abs/2405.01558" target="_blank">
  Zhan, Y., Shi, L., Matusik, W., Sun, Q., & Akşit, K. Configurable Learned Holography.
  </a>" <i>arXiv e-prints</i>
</p>
<!-- 
In comparison for our method, we only need one model to adapt to as many displays as you want 
and the model will give you single and multicolour hologram for each display settings. 
The network automatically adapts to it so multiple optical configurations are supported 
and because we are using distillation the network can support up to 25 FPS for HD resolution and it only requires requires RGB only 2D image as input.
-->

---
transition: fade-out
---

# Result:

<script setup>
import { ref } from 'vue'

const playbackRate = ref(0.7)
</script>

<div v-click="0">
  <div style="max-height: 320px; max-width: 320px;">
    <SlidevVideo v-click="0" autoplay autoreset :playbackRate="playbackRate" loop>
      <source src="/projects/Configurable_holo/test.mp4" type="video/mp4" />
    </SlidevVideo>
  </div>

  <div class="absolute left-105px top-445px text-center" style="background-color: #3cff19; max-height: 300px; max-width: 330px; padding: 2px 5px; z-index: 4;">
    <div class="relative inline-block">
      <span style="color: black; font-size:0.8em"><b>Pixel Pitch changing (8 - 10 μm)</b></span><br>
    </div>
  </div>
</div>

<div v-click="0">
  <div class="absolute right-105px top-95px text-center">
    <div style="max-height: 320px; max-width: 320px;">
      <SlidevVideo v-click="0" autoplay autoreset :playbackRate="playbackRate" loop>
        <source src="/projects/Configurable_holo/test2.mp4" type="video/mp4" />
      </SlidevVideo>
    </div>
  </div>
  <div class="absolute right-145px top-445px text-center" style="background-color: #3cff19; max-height: 300px; max-width: 330px; padding: 2px 5px; z-index: 4;">
    <div class="relative inline-block">
      <span style="color: black; font-size:0.8em"><b>Defocus Blur changing (4 - 8 mm)</b></span><br>
    </div>
  </div>
</div>

<div v-click="0">
  <div class="absolute right-468px top-250px text-center" style="background-color: #3cff19; max-height: 300px; max-width: 330px; padding: 2px 5px; z-index: 4;">
    <div class="relative inline-block">
      <span style="color: black; font-size:0.8em"><b>REAL TIME!</b></span><br>
    </div>
  </div>
</div>

<div v-click="0" class="absolute left-85px bottom-25px" style="width: 80%; z-index: 10;">
  <div class="flex justify-between text-xs mb-1">
    <span>Slow (0.5x)</span>
    <span>Normal (1x)</span>
    <span>Fast (2x)</span>
  </div>
  <input 
    type="range" 
    v-model="playbackRate" 
    min="0.5" 
    max="2" 
    step="0.01" 
    class="slider"
    style="width: 100%;"
  >
</div>

<p class="citation" style="font-size: 7px; position: absolute; right: 316px; bottom: -10px; z-index: 10;">
  (3) "<a rel="noopener noreferrer" href="https://arxiv.org/abs/2405.01558" target="_blank">
  Zhan, Y., Shi, L., Matusik, W., Sun, Q., & Akşit, K. Configurable Learned Holography.
  </a>" <i>arXiv e-prints</i>
</p>

<style>
.slider {
  -webkit-appearance: none;
  width: 100%;
  height: 10px;
  border-radius: 5px;
  background: #d3d3d3;
  outline: none;
  opacity: 0.7;
  -webkit-transition: .2s;
  transition: opacity .2s;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background: #3cff19;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: #3cff19;
  cursor: pointer;
}
</style>

<!-- 
Besides brightness level changing our network also supports pixel pitch and volume depth changing in real time.
We start with the left video first, now if I slow the video down you can see that when pixel pitch changes from 8 µm to 10 micro meters, the defocus effect of the grape is becoming smaller. This is because when the pixel size increases the diffraction angle of the light when it passes the pixel will decrease so the defocus effect will decrease as well,


On the right hand side, when the volume depth changes from 4 mm to 8 mm. The defocus effect will be bigger. 
This is because the volume depth represent the distance of the light propagation. 
Larger VD means larger light propagation distances in space so the light will diffract more, these changings can be viewed clearly when I speed up the video .
-->
