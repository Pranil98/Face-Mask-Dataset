# Face-Mask-Detector


I have developed this face mask detector using 1500 images with and without mask pics taken from internet and done some augmentation methods in images.I trained the neural network using SSD_MobileNet_V1 from TFOD zoo model in google colab with Tesla processor

It tooks 1 hour 10 min in google colab with 20000 epochs and then tested in my local system.

1. Setup your environment and installed the packages required ,briefly provided in tfod_setup file.

<p align="center">
<img src="https://github.com/Pranil98/Face-Mask-Detector/blob/master/Screenshots/1.PNG" alt="command">
</p>


## Note  Follow tfod_setup instructions till Step-16 bcoz Step-17 is training in local system and u can perform below lines for faster training in Google Colab.
2. I have trained in google colab so for that you have to mount your google drive in google colab and in google drive upload the file content of models 

   Steps in google colab
   
a.  %tensorflow_version 1.x     
b.   import os   
RESEARCH_DIR = "/content/drive/My Drive/PATH_TO_TFOD/tfod/models-1.13.0/research"         #Provide your path

c.  os.chdir(RESEARCH_DIR)
d.  os.getcwd()
e.  This is training code in python 
      !python train.py --logtostderr --train_dir=training/ --pipeline_config_path=training/ssdlite_mobilenet_v1_coco.config
f.  Copy and paste following code in your browser console(To open console Press Ctrl+Shift+I and paste it) to prevent Google                   Colab from terminating- JS code1-
   
      function ClickConnect(){
      console.log("Working"); 
      document.querySelector("colab-toolbar-button").click() 
      }setInterval(ClickConnect,60000)
      


<p align="center">
<img src="https://github.com/Pranil98/Face-Mask-Detector/blob/master/Screenshots/colabOutPut.png" alt="command">
</p>


<p align="center">
<img src="https://github.com/Pranil98/Face-Mask-Detector/blob/master/Screenshots/trainingStartedinColab.jpeg" alt="command">
</p>



3.After training is done in Colab then checkpoint files are created in Training folder in Models\Research\Training.Download and replace in your local system for generating .pb file from ckpt file and then further testing.

<p align="center">
<img src="https://github.com/Pranil98/Face-Mask-Detector/blob/master/Screenshots/drive.jpeg" alt="command">
</p>

4. Then you can proceed from Step-18 in tfod_setup file and convert ckpt files into pb file and then run your object detection tutorial file and can test images.

<p align="center">
<img src="https://github.com/Pranil98/Face-Mask-Detector/blob/master/Screenshots/test.PNG" alt="command">
</p>

** Contact me ps4798@rediffmail.com




   
