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
games_images=[rock, paper, scissors]
user_choice=int(input("What do you want to chose? Type 0 for rock, 1 for paper or 2 for scissors."))
if user_choice>=3 or user_choice<0:
  print("You typed an invalid number. You lose!")
print(games_images[user_choice])
computer_choice=random.randint(0,2)
print("Computer_chose:")
print(games_images[computer_choice])
if user_choice==0 and computer_choice==2:
  print("You win!")
elif computer_choice==0 and user_choice==2:
  print("You lose")
elif computer_choice>user_choice:
  print("You lose")
elif user_choice>computer_choice:
  print("Youo win!")
elif computer_choice==user_choice:
  print("Its a draw")      
