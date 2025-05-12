# Python-Projects
I am sharing a code of my python project of health management exercise where i have created a diet and exercise plan for three individuals and also logeed the time of their diet and xercise using the time module kindly find the code below:

def getdate():
    import datetime
    return datetime.datetime.now()
print("health management system")
num0 = int(input("press 1 for log the value and 2 for retrieve\n"))

def log(num1):
    if num1==1:
        num2 = int(input("what do you want to log, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            e=input("type here\n")
            with open ("1 - harry exercise.py", "a") as f:
                f.write(str([str(getdate())])+": "+e+"\n")
            print("successfully written")
        elif num2==2:
            e=input("type here\n")
            with open("1 - harry diet.py", "a") as f:
                f.write(str([str(getdate())])+": "+e+"\n")
            print("successfully written")
    elif num1==2:
        num2 = int(input("what do you want to log, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            e=input("type here\n")
            with open ("1 - rohan exercise.py", "a") as f:
                f.write(str([str(getdate())])+": "+e+"\n")
            print("successfully written")
        elif num2==2:
            e=input("type here\n")
            with open("1 - rohan diet.py", "a") as f:
                f.write(str([str(getdate())]) + ": "+e+"\n")
            print("successfully written")
    elif num1==3:
        num2 = int(input("what do you want to log, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            e=input("type here\n")
            with open ("1 - hammad exercise.py", "a") as f:
                f.write(str([str(getdate())])+": "+e+"\n")
            print("successfully written")
        elif num2==2:
            e=input("type here\n")
            with open("1 - hammad diet.py", "a") as f:
                f.write(str([str(getdate())]) + ": "+e+"\n")
            print("successfully written")
    else:
        print("invalid entry, please enter 1,2 or 3")

def retrieve(num1):
    if num1==1:
        num2=int(input("hat do you want to retrieve, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            with open ("1 - harry exercise.py") as f:
                for i in f:
                    print(i,end=" ")
        elif num2==2:
            with open ("1 - harry diet.py") as f:
                for i in f:
                    print(i,end=" ")
    elif num1==2:
        num2=int(input("hat do you want to retrieve, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            with open ("1 - rohan exercise.py") as f:
                for i in f:
                    print(i,end=" ")
        elif num2==2:
            with open ("1 - rohan diet.py") as f:
                for i in f:
                    print(i,end=" ")
    elif num1==3:
        num2=int(input("hat do you want to retrieve, press 1 for exercise and 2 for diet\n"))
        if num2==1:
            with open ("1 - hammad exercise.py") as f:
                for i in f:
                    print(i,end=" ")
        elif num2==2:
            with open ("1 - hammad diet.py") as f:
                for i in f:
                    print(i,end=" ")
    else:
        print("invalid entry, please enter 1,2 or 3")

if num0==1:
    num1 = int(input("Enter the name of client,1 = harry,2 = rohan or 3 = hammad\n"))
    log(num1)
elif num0==2:
    num1 = int(input("Enter the name of client,1 = harry,2 = rohan or 3 = hammad\n"))
    retrieve(num1)
