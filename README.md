# RPS
import random
lst = ['R','P','S']

chance = 10
no_of_chance = 0
computer_point = 0
human_point = 0

print(" \t \t \t \t Rock,Paper,Scissor Game\n \n")
print("R for Rock \nP for Paper \nS for Scissor \n")

# making the game in while
while no_of_chance < chance:
    _human = input('Enter R,P,S any one:')
    _computer = random.choice(lst)

    if _human == _computer:
        print(f"your guess {_human} and computer is {_computer}\n")
        print("Tie Both 0 point to each \n ")
        print(f"computer_point is {computer_point} and your_point is {human_point}\n")

    # if user enter R
    elif _human == "R" and _computer == "P":
        computer_point = computer_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("computer wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n ")

    elif _human == "R" and _computer == "S":
        human_point = human_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("Human wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n")

    # if user enter P
    elif _human == "P" and _computer == "S":
        computer_point = computer_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("computer wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n ")

    elif _human == "P" and _computer == "R":
        human_point = human_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("Human wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n")

    # if user enter S

    elif _human == "S" and _computer == "P":
        human_point = human_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("Human wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n")


    elif _human == "S" and _computer == "R":
        computer_point = computer_point + 1
        print(f"your guess {_human} and computer guess is {_computer} \n")
        print("computer wins 1 point \n")
        print(f"computer_point is {computer_point} and your point is {human_point} \n ")

    else:
        print("you have input wrong \n")

    no_of_chance = no_of_chance + 1
    print(f"{chance - no_of_chance} is left out of {chance} \n")

print("Game over")

if computer_point==human_point:
    print("Tie")

elif computer_point > human_point:
    print("Computer wins and you loose")

else:
    print("you win and computer loose")

print(f"your point is {human_point} and computer point is {computer_point}")
