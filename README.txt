Quoc Cao
EE104
Lab#6

Reference: Laboratory Assignment 7

***Github: https://github.com/Quoccao1/Balloon-Flight-game.git
***Video link for the Balloon Flight: https://youtu.be/fjk90VRRcco
***Video link for the images recognize demonstration: https://youtu.be/YPcKq5HIRl8

***MAKE SURE THAT THE FOLLOWING PYTHON MODULES ARE INSTALLED***
import pgzrun
import pygame
import pgzero
from pgzero.builtins import Actor
from random import randint
import smtplib, ssl
import time
from sys import exit

**Images recognize
-Following the instruction in the Laboratory Assignment 7 to install and set up all of the necessary things for the Image recognizer
-Add a minimum 15-30 pictures of a new object and yourself (add many picture as you want to increase the accuracy)
-Label all the pictures that you added in the folder
-Train the model with your own images
-Open a Powershell window (Run as administrator) and run the commands below
***Note: Do a trial run with epochs=20 first, then change the number of epochs to as high as your time permits, i.e. epochs=100***
*yolo task=detect mode=train model=C:/ultralytics/ultralytics/models/v8/yolov8n.yaml data=C:/ultralytics/ultralytics/datasets/datasets/coco128_ee104.yaml epochs=20
-Then,
*yolo task=detect mode=train model=C:/ultralytics/ultralytics/models/v8/yolov8n.yaml data=C:/ultralytics/ultralytics/datasets/datasets/coco128_ee104.yaml epochs=100
-After it done, the last line of the output shows where the result is saved EX: c:\ultralytics\runs\detect\train
-Then, you will use your own best.pt model that you just trained to test the webcam
-Here is the command to detect from the computer USB webcam: yolo task=detect mode=predict model=C:/ultralytics/runs/detect/train/weights/best.pt source=0 show=True 
(***Make sure to change to your own directory***)

**Game Balloon Flight
-Add hacks and tweaks:Lives, More High Scores, File Handling, Level Up, Space out the Obstacles. 
-Modifying the code as we want
-Run and enjoy the game