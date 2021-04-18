# Multifunctional-door-lock-based-on-face-recognition
## Table of content
<ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li><a href="#get-start">Get Start</a></li>
    <li><a href="#main-functions">Main functions</a</li>
    <li><a href="#operation">Operation</a></li>
    <li><a href="#run">Run</a></li>
    <li><a href="#contact">Contact</a></li>
</ol>

## About the project
This project is a multifunctional door lock based on face recognition, and we added some interesting and useful functions on this project.

## Get Start
* Hardware：<br>
    `Raspberry pi 4b `<br>
               ` Camera with CSI interface` <br>
               `HC-SR 501 RD-624`<br>
               `lock`
               `LED(3W)`<br>
               `buzzer`<br>
               `flame monitor`<br>
               `relay`
               `breadboard` <br>
               `some dupont line` <br>
           
* software: <br>
           `linux`
           
## Main functions
 * Face recognition<br>
  Our project apply NCNN nerual network framework, it is a high-performance framwork for competing and inference, and face detection method we used is mtcnn.
   It's worth mentioning that we added anti-spoofig function, which can detect whether the face from the camera is real to make sure that our camera won't be 
   cheat by fake face, like faces in photos and screens.<br>
 * Infrade detection and add new face<br>
     When people's face is close to the camera,the red LED shine and it start to detect whether the face is in the existing face repository, 
     if it exists, then send true signal, otherwise it is False signal, we can add more faces to the repository by pressing the button in real time<br>
 * control of lock<br>
    When the raspberry Pi detect the face in the repository, it will send the true signal and the lock will open automatically, we can close the lock after detection.<br>
  * flame monitor and buzzer<br>
    in order to improve the safety performance of our project, we add this part. When the flame monitor detect the fire, the buzzer will make noise to remind people that there's a fire<br>
    
    
## Operation
   * preparation<br>
   OPENCV>=4.0.0<br>
   * project_path<br>
   set 'project_path' in livefacereco.hpp into your own<br>
   
   
## Run
  mkdir build<br>
  cd build<br>
  cmake ..<br>
  make -j4<br>
  ./LiveFaceReco<br>
 ## Contact
 Xianglong Cheng(2594921C)<br>
 Wenyi Li(2520495L)<br>
 Fan Zou(2596373Z)<br>