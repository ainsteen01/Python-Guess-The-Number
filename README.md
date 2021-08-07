# Python-Guess The Number.
# Try in Google colab Notebook..
import os
import time
import random
from google.colab import output
print (f"""\rScore = {scr}                                  Life  = {life}
""")
 lvl=5
while life > 0:
    print (" ---- Enter a Number between 1 and " , lvl)
    ai = random.randint(1,lvl)
   # print(ai)
    print("\n")
    pre = int(input ("Enter num: "))
    if pre == ai:
        print(f'***CORRECT***')
        time.sleep(1)
        scr+=1
        if scr > pnt:
            lvl = lvl+2
            life = life+2
            pnt = pnt+511
    elif pre != ai:
        life-=1
    
    
    output.clear()
    print (f"""\rScore = {scr}                                  Life  = {life}
           
           Your Prediction = {pre}                        Machine Prediction = {ai}""")
    if life == 0:
      print("\n")
      print("              <<<<<<<< GAME OVER >>>>>        ")
