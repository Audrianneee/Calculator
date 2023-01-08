# Calculator

import math
import os

def menu():
  global op
  print("Welcome to advance calculator !")
  print("1. Addition")
  print("2. Substraction")
  print("3. Division")
  print("4. Multiplication")
  print("5. Square root")
  print("6. Square")
  print("7. Cubic root")
  print("8. Cubic")
  try:
    op=int(input("Choose the operation : "))
  except ValueError:
    print("Input a number")


def add(a,b):
  hasil=a+b
  print("hasil =",hasil)

def minus(a,b): 
  hasil=a-b
  print("hasil =",hasil)

def div(a,b):
  try:
    hasil=a/b
    print("hasil=",hasil)
  except ZeroDivisionError:
    print("Pembagian dengan nol")

def mul(a,b):
  hasil=a*b
  print("hasil",hasil)

def s(a):
  hasil=a**2
  print("hasil",hasil)

def sr(a):
  hasil=math.sqrt(a)
  print("hasil",hasil)

def cr(a):
  hasil=a**(1/3)
  print("hasil",hasil)

def c(a):
  hasil=a**3
  print("hasil",hasil)

while True:
  menu()
  if 1<=op<=4:
    while True:
      try:
        a=int(input("1st number : "))
        break
      except ValueError:
        print("Input a number")
    while True:
      try:
        b=int(input("2nd number : "))
        break
      except ValueError:
        print("Input a number")   
    if op==1:
      add(a,b)
    elif op==2:
      minus(a,b)
    elif op==3:
      div(a,b)
    elif op==4:
      mul(a,b)

  elif 5<=op<=8:
    while True:
      try:
        a=int(input("Input number : "))
        break
      except ValueError:
        print("Input a number")
    if op==5:
      sr(a)
    elif op==6:
      s(a)
    elif op==7:
      cr(a)
    elif op==8:
      c(a)
  
  yn=input("Do you want to calculate another number?(y/n): ")
  if yn=="y":
    os.system("clear")
  elif yn=="n":
    break
