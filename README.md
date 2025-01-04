# python-rock-paper-scissors-game-
import random
choose= ['r','p','s']
your_score =0
computer_score =0
def game():

  while True:
    global your_score, computer_score
    print("if you want to quit the game type 'fuck'")
    print("if you want to know you score enter 'score'")
    com=random.choice(choose)
    me=input("choose one (rock = r , paper = p , scissor = s): ")
    if me==com:
      print("tie")
      game()
    elif me=='r' and com=='s':
      print("you win")
      your_score+=1
      game()
    elif me=='r' and com=='p':
      print("you lose")
      computer_score+=1
      game()
    elif me=='p' and com=='r':
      print("you win")
      your_score+=1
      game()
    elif me=='p' and com=='s':
      print("you lose")
      computer_score+=1
      game()
    elif me=='s' and com=='r':
      print("you lose")
      computer_score+=1
      game()
    elif me=='s' and com=='p':
      print("you win")
      your_score+=1
      game()
    elif me=='score':
      print("your score is: ",your_score)
      print("computer score is: ",computer_score)
      continue
    elif me=='fuck':
      print("your final score is",your_score,"and computer score is",computer_score)
      your_score = 0
      computer_score = 0
      break
    else:
      print("invalid input")
      print(f"your points are {your_score} and computers points are {computer_score}")
      continue

game()
