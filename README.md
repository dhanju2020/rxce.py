#!/usr/bin/python
# -*- coding: UTF-8 -*-
from os import system, name
import itertools
import threading
import time
import sys
import datetime
from base64 import b64decode,b64encode
from datetime import date

expirydate = datetime.date(2021, 12, 27)
expirydate = datetime.date(2021, 12, 31)
#expirydate = datetime.date(2021, 12, 31)
today=date.today()
def hero():
    def chalo():
        done = False
        #here is the animation
        def animate():
            for c in itertools.cycle(['|', '/', '-', '\\']) :
                if done:
                    break
                sys.stdout.write('\rhacking in the server for next colour--------- ' + c)
                sys.stdout.flush()
                time.sleep(0.1)
            sys.stdout.write('\rDone!     ')
        t = threading.Thread(target=animate)
        t.start()
        #long process here
        time.sleep(20)
        done = True
    def chalo1():
        done = False
        #here is the animation
        def animate():
            for c in itertools.cycle(['|', '/', '-', '\\']):
                if done:
                    break
                sys.stdout.write('\rgetting the colour wait --------- ' + c)
                sys.stdout.flush()
                time.sleep(0.1)
            sys.stdout.write('\rDone!     ')
        t = threading.Thread(target=animate)
        t.start()
        #long process here
        time.sleep(20)
        done = True
    def clear():
        # for windows
        if name == 'nt':
            _ = system('cls')
        # for mac and linux(here, os.name is 'posix')
        else:
            _ = system('clear')
    def getSum(n):
        sum=0
        for digit in str(n):
            sum+= int(digit)
        return sum
    def lawde_time_pe_khel(n):
        check=0
        for digit in (n):
            if(int(digit)==0):
                check=check+1
        return check
    clear()
    y=1
    newperiod=period
    banner='figlet AMUSEBOX'
    numbers=[]
    while(y):
        clear()
        system(banner)
        print("Contact")
        print("Enter ",newperiod," Parity Price :")
        current=input()
        current=int(current)
        chalo()
        print("\n---------Successfully hacked the server-----------")
        chalo1()
        print("\n---------Successfully got the colour -------------")
        print('\n')
        last2=str(current)[-2:]
        Timeout(last2)
        if(newperiod%2==0):
            sum=getSum(current)
            if(sum%2==0):
                print(newperiod+1," : 🔴, RED")
            else:
                print(newperiod+1,"  : 🟢, GREEN")
        else:
            sum=getSum(current)
            if(sum%2==0):
                print(newperiod+1,"   : 🔴, RED")
            else:
                print(newperiod+1,"   : 🟢, GREEN")
        newperiod+=1
        numbers.append(current)
        y=input("Do you want to play : Press 1 and 0 to exit \n")
        if(y==0):
            y=False
        if (len(numbers)>11):
            clear()
            system('figlet Thank you!!')
