# Finding-Screen-coordinates

#  Finding Screen Coordinates using python 
# You have to just click on the screen where you want to find the coordinates

from pynput.mouse import Controller,Button,Listener
from pynput.keyboard import Controller as KeyboardController
from numpy import asarray
from mss import mss
import cv2
import time

def on_click(x, y, button, pressed):
     if pressed:
         print('X:{0}, Y:{1}'.format(x, y))

with Listener(on_click=on_click) as listener:
     listener.join()
