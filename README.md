# Smart-Street-Light-Using-Raspberry-pi-

import RPi.GPIO as IO
import time
IO.setwarnings(False)
IO.setmode(IO.BCM)
IO.setup(2,IO.OUT)
IO.setup(3,IO.OUT)
IO.setup(14,IO.IN)
IO.setup(17,IO.IN)
while 1:
    if(IO.input(14)==True):
        IO.output(2,True)
    if(IO.input(14)==False):
        IO.output(2,False)
    if(IO.input(17)==True):
        IO.output(3,True)
    if(IO.input(17)==False):
        IO.output(3,False)
