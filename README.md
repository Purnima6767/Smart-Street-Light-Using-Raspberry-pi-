# Smart-Street-Light-Using-Raspberry-pi-
overview:-
 "An Automatic smart street light using raspberry pi is an intelligent system of street light which minimizes the problem of electricity power consumption which is caused late at night when the streets are working. The system is designed using LED, IR sensor, SD card, with all these components which are connected and controlled using raspberry pi. This system will detect the vehicle and it turns the street light to full intensity when the vehicle passes and the street lights are automatically tuned to low intensity if not required."

Program for interfacing::-
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
