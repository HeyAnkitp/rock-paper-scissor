# rock-paper-scissor
rock papr scissor pyton code



import random
rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
game_images = [rock, paper, scissors]
user_choice = int(input("type 0:rock, 1:papper, 2:scissors \n"))

if user_choice >= 3 or user_choice < 0:
  print("you type a invalid number, you lose")
else:  
  print(game_images[user_choice])
  
  computer_choice = random.randint(0,2)
  print("computer chose")
  print(game_images [computer_choice])
  
  
  if user_choice == 0 and computer_choice == 2:
    print("you win") 
  elif user_choice == 2 and computer_choice == 0:
    print("you lose")
  
  elif computer_choice > user_choice:
    print("you lose")
  elif user_choice > computer_choice:
    print("you win")
  elif user_choice == computer_choice:
    print("it's a draw")
