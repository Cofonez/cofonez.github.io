## Below is some examples of python projects that i've been working on in my spare time





```markdown
##Python Code Projects

#establishing some variables that we will increment
#for whenever we find an integer that fits the criteria
less = 0
greater = 0
equal = 0
counter = 0

import random 

#code = [random.randint(0,9),random.randint(0,9),random.randint(0,9),random.randint(0,9)]

code=""
for r in range(4):
    x=random.randint(1,9)
    x =str(x)
    code = code+x


guess = input("enter your 4 digit guess: ")

if '0' in guess:
    print(code)

#error handling for entries less than or greater than 4
if len(guess) != 4:
    guess =input("The code is 4 numbers long, please only enter 4 digits: ")
    

#error handling for non numeric input
if guess.isdigit() == False:
    guess = input("Please only enter digits: ")

done = False
while not done:
    while equal != 4:
        while counter < len(code):
            if code[counter]==guess[counter]:
                equal+=1
            elif code[counter] > guess[counter]:
                greater+=1
            else:
                less += 1
            counter += 1
            if equal == 4:
                print("congratulations you guessed the code correctly")
                done = True
            
        if equal != 4:
            print("Your clue is" + "=" * equal + "<" * less + ">" *greater)
            less=0
            greater=0
            counter=0
            equal=0
            guess = input("enter your 4 digit guess: ")
            if '0' in guess:
                print(code)



##Conversion project
#constants for conversions
gpp = 453.592
cpi = 2.54
kpm = 1.60934

print("Enter Desired Conversion")
print("------------------------")
print("1 - pounds/grams")
print("2 - inches/centimeters")
print("3 - miles/kilometers")

#input for the conversion selection
choice = (input("enter: "))

#setting beggining flag for repeating conversions with the variable more

more = True


while more == True:
    

    #error handling for cases that are not 1 2 or 3
    while choice not in ('1','2','3'):
              print("invalid input")
              choice = (input("enter: "))

    #case 1
    if choice == '1':


    #when selection is made establish which direction they want to convert
    #error handling here
        selection = input("pounds to grams (a), or grams to pounds (b)?")
        while selection not in ('a','b'):
                print("invalid selection")
                selection = input("pounds to grams (a), or grams to pounds (b)?")
        if selection == 'a':
            conv = int(input("enter the number of pounds: "))
            result = gpp*conv
            print((conv," pounds is equal to",format(result,'.2f'),"grams"))
        if selection == 'b':
            conv = int(input("enter the number of grams: "))
            result = conv/gpp
            print((conv," grams is equal to",format(result,'.2f'),"pounds"))
            #variable for more conversions
           

    #case 2
    if choice == '2':

    #when selection is made establish which direction they want to convert
    #error handling here
        selection = input("inches to centimeters (a), or centimeters to inches (b)?")
        while selection not in ('a','b'):
                print("invalid selection")
                selection = input("inches to centimeters (a), or centimeters to inches (b)?")
        if selection == 'a':
            conv = int(input("enter the number of inches: "))
            result = cpi*conv
            print((conv," inches is equal to",format(result,'.2f'),"centimeters"))
        if selection == 'b':
            conv = int(input("enter the number of centimeters: "))
            result = conv/cpi
            print((conv," centimeters is equal to",format(result,'.2f'),"inches"))

    #case 3
    if choice == '3':

    #when selection is made establish which direction they want to convert
    #error handling here
        selection = input("miles to kilometers (a), or kilometers to miles (b)?")
        while selection not in ('a','b'):
                print("invalid selection")
                selection = input("miles to kilometers (a), or kilometers to miles (b)?")
        if selection == 'a':
            conv = int(input("enter the number of miles: "))
            result = kpm*conv
            print((conv," miles is equal to",format(result,'.2f'),"kilometers"))
        if selection == 'b':
            conv = int(input("enter the number of kilometers: "))
            result = conv/kpm
            print((conv," kilometers is equal to",format(result,'.2f'),"meters"))

            
    ask = input("do you wish to do another conversion (y/n): ")
    #asking for more conversions
    while ask not in ('y','n','Y','N'):
        print("invalid input")
        ask = input("do you wish to do another conversion (y/n): ")
    if ask in ('N','n'):
        print("Goodbye")
        more = False

###More Examples can be found in my repositories page
