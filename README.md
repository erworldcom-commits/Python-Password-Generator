# Python-Password-Generator
Hello welcome in password generator machine
you can test it here 
https://www.programiz.com/online-compiler/5KUiaHf9U1e4D

import random

letters_list = [
    'a','B','C','d','e','F','g','h','I3'
    '','j',
    'k','L','m','n','o','p','Q','r','s','T',
    'U','V','w','X','Y'
]

numbers_list = ['0','1','2','3','4','5','6','7','8','9']

symbols_list = [
    '!','@','#','$','%','^','&','*','(',')',
    '-','_','+','=',
    ':',';','<','>','?']

print("Welcome to Password Generator Program")

nr_letters = int(input("How many letters would you like?\n"))
nr_symbols = int(input("How many symbols would you like?\n"))
nr_numbers = int(input("How many numbers would you like?\n"))

password_list= []

for _ in range(nr_letters):
    password_list.append (random.choice(letters_list))

for _ in range(nr_symbols):
    password_list.append(random.choice(symbols_list))

for _ in range(nr_numbers):
    password_list.append(random.choice(numbers_list))

print(password_list)
random.shuffle(password_list)
print(password_list)
password = ""
for char in password_list:
    password+= char
print(f"Your password is: {password}")
