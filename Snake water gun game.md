I am sharing a code of my python project of health management exercise where i have created a diet and exercise plan for three individuals and also logeed the time of their diet and xercise using the time module kindly find the code below:
import random
list1 = ["snake", "water", "gun"]

human_points = 0
computer_points = 0
print("let the game begins, you have ten attempts")
number_of_attempts = 1
while number_of_attempts<=10:
    user_choice = input("Enter snake, water or gun\n")
    com_choice = random.choice(list1)
    if user_choice == com_choice:
        print("it's a draw, try again\n")
#if user chooses snake
    elif user_choice=="snake" and com_choice=="gun":
        computer_points = computer_points + 1
        print("you lose computer chose", com_choice,"computer", computer_points, "and human = ", human_points, "try again\n")
    elif user_choice=="snake" and com_choice=="water":
        human_points = human_points + 1
        print("you won computer chose", com_choice,"computer",computer_points, "and human = ", human_points, "try again\n")
#if user chooses water
    elif user_choice=="water" and com_choice=="snake":
        computer_points = computer_points + 1
        print("you lose computer chose", com_choice,"computer", computer_points, "and human = ", human_points, "try again\n")
    elif user_choice=="water" and com_choice=="gun":
        human_points = human_points + 1
        print("you won computer chose", com_choice,"computer",computer_points, "and human = ", human_points, "try again\n")
# if user chooses gun
    elif user_choice=="gun" and com_choice=="water":
        computer_points = computer_points + 1
        print("you lose computer chose", com_choice,"computer", computer_points, "and human = ", human_points, "try again\n")
    elif user_choice=="gun" and com_choice=="snake":
        human_points = human_points + 1
        print("you won computer chose", com_choice,"computer",computer_points, "and human = ", human_points, "try again\n")
    else:
        print("invalid input")
    print(10 - number_of_attempts, "number of attempts remaining")
    number_of_attempts = 1 + number_of_attempts

if number_of_attempts>10:
    print("game over")
    print("computer_points", computer_points)
    print("human points", human_points)
if computer_points>human_points:
    print("Sorry computer won")
elif computer_points==human_points:
    print("it is a tie")
elif human_points>computer_points:
    print("congratulations you won")



# while (user_choice<10):
#     print(user_choice)
#     user_choice = user_choice+1




