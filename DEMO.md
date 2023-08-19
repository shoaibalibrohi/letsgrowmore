# Demo

### PROJECT-1 Band Generator name

```python

print("Welcome to band generator\n")
city =input("Enter the city you grew up\n")
pet_name = input("Enter your pet name\n")
print(city+" "+ pet_name)
```
[Run this project](https://band-name-generator-end.appbrewery.repl.run/) 
___


### PROJECT-2 TIP CALCULATOR
```python
print("welcome to tipcalculator")
bill=int(input("What was total bill$ ?\n"))
tip_percent=float(input("What percentage tip would you like to give 10%, 12% or 15% ?  \n"))
distribution=int(input("How many people to split the bill?\n"))
tip=(bill/distribution)*(1+(tip_percent/100))
ftip= round(tip,2)
print(f"Each person should pay" + ftip)
```
[Run this project](https://replit.com/@Aristo00071/tip-calculator-start#main.py/) 
___


### PROJECT-3 Treasure-ISLAND

```python

                    print('''
                    *******************************************************************************
                              |                   |                  |                     |
                     _________|________________.=""_;=.______________|_____________________|_______
                    |                   |  ,-"_,=""     `"=.|                  |
                    |___________________|__"=._o`"-._        `"=.______________|___________________
                              |                `"=._o`"=._      _`"=._                     |
                     _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
                    |                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
                    |___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
                              |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
                     _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
                    |                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
                    |___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
                    ____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
                    /______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
                    ____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
                    /______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
                    ____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
                    /______/______/______/______/______/______/______/______/______/______/_____ /
                    *******************************************************************************
                    ''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.")
choice1 = input('You\'re at a cross road. Where do you want to go? Type "left" or "right" \n').lower()
if choice1 == "left":
  choice2 = input('You\'ve come to a lake. There is an island in the middle of the lake. Type "wait" to wait for a boat. Type "swim" to swim across. \n').lower()
  if choice2 == "wait":
    choice3 = input("You arrive at the island unharmed. There is a house with 3 doors. One red, one yellow and one blue. Which colour do you choose? \n").lower()
    if choice3 == "red":
      print("It's a room full of fire. Game Over.")
    elif choice3 == "yellow":
      print("You found the treasure! You Win!")
    elif choice3 == "blue":
      print("You enter a room of beasts. Game Over.")
    else:
      print("You chose a door that doesn't exist. Game Over.")
  else:
    print("You get attacked by an angry trout. Game Over.")
else:
  print("You fell into a hole. Game Over.")
  ```
  
[Run this project]https://replit.com/@Aristo00071/treasure-island-end#main.py) 
  
  ___

### PROJECT-4 ROCK PAPER SCISSORS
```python
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
game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors.\n"))
print(game_images[user_choice])

computer_choice = random.randint(0, 2)
print("Computer chose:")
print(game_images[computer_choice])

if user_choice >= 3 or user_choice < 0: 
  print("You typed an invalid number, you lose!") 
elif user_choice == 0 and computer_choice == 2:
  print("You win!")
elif computer_choice == 0 and user_choice == 2:
  print("You lose")
elif computer_choice > user_choice:
  print("You lose")
elif user_choice > computer_choice:
  print("You win!")
elif computer_choice == user_choice:
  print("It's a draw")
  
```
[Run this project](https://replit.com/@Aristo00071/rock-paper-scissors-start#main.py) 

___


### PROJECT-5 Password Generator Project

```python

#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters = int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

password_list = []

for char in range(1, nr_letters + 1):
  password_list.append(random.choice(letters))

for char in range(1, nr_symbols + 1):
  password_list += random.choice(symbols)

for char in range(1, nr_numbers + 1):
  password_list += random.choice(numbers)


random.shuffle(password_list)


password = ""
for char in password_list:
  password += char

print(f"Your password is: {password}")
```
[Run this project](https://replit.com/@Aristo00071/password-generator-end#main.py) 
___


### PROJECT-6 Automating Robot

>automating robot to find way to reach destination.  
>Please go through [this link](https://reeborg.ca/reeborg.html?lang=en&mode=python&menu=worlds%2Fmenus%2Freeborg_intro_en.json&name=Maze&url=worlds%2Ftutorial_en%2Fmaze1.json)
___


### PROJECT-7 Hangman


```python
                               _                                             
                              | |                                            
                              | |__   __ _ _ __   __ _ _ __ ___   __ _ _ __  
                              | '_ \ / _` | '_ \ / _` | '_ ` _ \ / _` | '_ \ 
                              | | | | (_| | | | | (_| | | | | | | (_| | | | |
                              |_| |_|\__,_|_| |_|\__, |_| |_| |_|\__,_|_| |_|
                                                  __/ |                      
                                                 |___/    '''

#Step 5

import random

#TODO-1: - Update the word list to use the 'word_list' from hangman_words.py
#Delete this line: word_list = ["ardvark", "baboon", "camel"]
from hangman_words import word_list

chosen_word = random.choice(word_list)
word_length = len(chosen_word)

end_of_game = False
lives = 6

#TODO-3: - Import the logo from hangman_art.py and print it at the start of the game.
from hangman_art import logo
print(logo)

#Testing code
print(f'Pssst, the solution is {chosen_word}.')

#Create blanks
display = []
for _ in range(word_length):
    display += "_"

while not end_of_game:
    guess = input("Guess a letter: ").lower()

    #TODO-4: - If the user has entered a letter they've already guessed, print the letter and let them know.
    if guess in display:
        print(f"You've already guessed {guess}")

    #Check guessed letter
    for position in range(word_length):
        letter = chosen_word[position]
        #print(f"Current position: {position}\n Current letter: {letter}\n Guessed letter: {guess}")
        if letter == guess:
            display[position] = letter

    #Check if user is wrong.
    if guess not in chosen_word:
        #TODO-5: - If the letter is not in the chosen_word, print out the letter and let them know it's not in the word.
        print(f"You guessed {guess}, that's not in the word. You lose a life.")
        
        lives -= 1
        if lives == 0:
            end_of_game = True
            print("You lose.")

    #Join all the elements in the list and turn it into a String.
    print(f"{' '.join(display)}")

    #Check if user has got all letters.
    if "_" not in display:
        end_of_game = True
        print("You win.")

    #TODO-2: - Import the stages from hangman_art.py and make this error go away.
    from hangman_art import stages
    print(stages[lives])
   
    
```
[Run this project](https://replit.com/@Aristo00071/Day-7-Hangman-5-End#hangman_art.py) 



### PROJECT-8 PASSWORD ENCRYPTER DECRYPTER

```python

                    logo = """           
                     ,adPPYba, ,adPPYYba,  ,adPPYba, ,adPPYba, ,adPPYYba, 8b,dPPYba,  
                    a8"     "" ""     `Y8 a8P_____88 I8[    "" ""     `Y8 88P'   "Y8  
                    8b         ,adPPPPP88 8PP"""""""  `"Y8ba,  ,adPPPPP88 88          
                    "8a,   ,aa 88,    ,88 "8b,   ,aa aa    ]8I 88,    ,88 88          
                     `"Ybbd8"' `"8bbdP"Y8  `"Ybbd8"' `"YbbdP"' `"8bbdP"Y8 88   
                                88             88                                 
                               ""             88                                 
                                              88                                 
                     ,adPPYba, 88 8b,dPPYba,  88,dPPYba,   ,adPPYba, 8b,dPPYba,  
                    a8"     "" 88 88P'    "8a 88P'    "8a a8P_____88 88P'   "Y8  
                    8b         88 88       d8 88       88 8PP""""""" 88          
                    "8a,   ,aa 88 88b,   ,a8" 88       88 "8b,   ,aa 88          
                     `"Ybbd8"' 88 88`YbbdP"'  88       88  `"Ybbd8"' 88          
                                  88                                             
                                  88           
                    """

alphabet = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

def caesar(start_text, shift_amount, cipher_direction):
	end_text = ""
	if cipher_direction == "decode":
		shift_amount *= -1
	for char in start_text:
		if char in alphabet:
			position = alphabet.index(char)
			new_position = position + shift_amount
			end_text += alphabet[new_position]
		else:
			end_text += char
	print(f"Here's the {cipher_direction}d result: {end_text}")

from art import logo
print(logo)
end=False
while not end:
	direction = input("Type 'encode' to encrypt, type 'decode' to decrypt:\n")
	text = input("Type your message:\n").lower()
	shift = int(input("Type the shift number:\n"))
	shift=shift%26
	caesar(start_text=text, shift_amount=shift,cipher_direction=direction)
	restart = input("Type 'yes' if you want to go again. Otherwise type 'no'.\n")
	if restart == "no":
		end=True
		print("Goodbye")
    
```

[Run this project]( https://replit.com/@Aristo00071/caesar-cipher-4-start#main.py) 

___
    


### PROJECT-8 BLIND AUCTION
```python

from replit import clear
from art import logo
print(logo)

bids = {}
bidding_finished = False

def find_highest_bidder(bidding_record):
  highest_bid = 0
  winner = ""
  # bidding_record = {"Angela": 123, "James": 321}
  for bidder in bidding_record:
    bid_amount = bidding_record[bidder]
    if bid_amount > highest_bid: 
      highest_bid = bid_amount
      winner = bidder
  print(f"The winner is {winner} with a bid of ${highest_bid}")

while not bidding_finished:
  name = input("What is your name?: ")
  price = int(input("What is your bid?: $"))
  bids[name] = price
  should_continue = input("Are there any other bidders? Type 'yes or 'no'.\n")
  if should_continue == "no":
    bidding_finished = True
    find_highest_bidder(bids)
  elif should_continue == "yes":
    clear()
  
```

[Run this project](https://replit.com/@Aristo00071/blind-auction-completed#main.py) 

___


### PROJECT-10 CALCULATOR USING DICTIONARY
```python

from replit import clear
from art import logo

def add(n1, n2):
  return n1 + n2

def subtract(n1, n2):
  return n1 - n2

def multiply(n1, n2):
  return n1 * n2

def divide(n1, n2):
  return n1 / n2

operations = {
  "+": add,
  "-": subtract,
  "*": multiply,
  "/": divide
}

def calculator():
  print(logo)

  num1 = float(input("What's the first number?: "))
  for symbol in operations:
    print(symbol)
  should_continue = True
 
  while should_continue:
    operation_symbol = input("Pick an operation: ")
    num2 = float(input("What's the next number?: "))
    calculation_function = operations[operation_symbol]
    answer = calculation_function(num1, num2)
    print(f"{num1} {operation_symbol} {num2} = {answer}")

    if input(f"Type 'y' to continue calculating with {answer}, or type 'n' to start a new calculation: ") == 'y':
      num1 = answer
    else:
      should_continue = False
      clear()
      calculator()

calculator()

```
[Run this project]( https://replit.com/@Aristo00071/calculator-final#main.py ) 

___



### PROJECT-11 BLACK JACK GAME

```python



############### Our Blackjack House Rules #####################

## The deck is unlimited in size. 
## There are no jokers. 
## The Jack/Queen/King all count as 10.
## The the Ace can count as 11 or 1.
## Use the following list as the deck of cards:
## cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
## The cards in the list have equal probability of being drawyn.
## Cards are not removed from the deck as they are drawn.



import random
from replit import clear
from art import logo

def deal_card():
  """Returns a random card from the deck."""
  cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
  card = random.choice(cards)
  return card


def calculate_score(cards):

  if sum(cards) == 21 and len(cards) == 2:
    return 0

  if 11 in cards and sum(cards) > 21:
    cards.remove(11)
    cards.append(1)
  return sum(cards)


def compare(user_score, computer_score):

  if user_score > 21 and computer_score > 21:
    return "You went over. You lose 😤"


  if user_score == computer_score:
    return "Draw 🙃"
  elif computer_score == 0:
    return "Lose, opponent has Blackjack 😱"
  elif user_score == 0:
    return "Win with a Blackjack 😎"
  elif user_score > 21:
    return "You went over. You lose 😭"
  elif computer_score > 21:
    return "Opponent went over. You win 😁"
  elif user_score > computer_score:
    return "You win 😃"
  else:
    return "You lose 😤"

def play_game():

  print(logo)

  user_cards = []
  computer_cards = []
  is_game_over = False

  for _ in range(2):
    user_cards.append(deal_card())
    computer_cards.append(deal_card())


  while not is_game_over:

    user_score = calculate_score(user_cards)
    computer_score = calculate_score(computer_cards)
    print(f"   Your cards: {user_cards}, current score: {user_score}")
    print(f"   Computer's first card: {computer_cards[0]}")

    if user_score == 0 or computer_score == 0 or user_score > 21:
      is_game_over = True
    else:
      user_should_deal = input("Type 'y' to get another card, type 'n' to pass: ")
      if user_should_deal == "y":
        user_cards.append(deal_card())
      else:
        is_game_over = True

  while computer_score != 0 and computer_score < 17:
    computer_cards.append(deal_card())
    computer_score = calculate_score(computer_cards)

  print(f"   Your final hand: {user_cards}, final score: {user_score}")
  print(f"   Computer's final hand: {computer_cards}, final score: {computer_score}")
  print(compare(user_score, computer_score))


while input("Do you want to play a game of Blackjack? Type 'y' or 'n': ") == "y":
  clear()
  play_game()
  
```

[Run this project]( https://replit.com/@Aristo00071/blackjack-start#main.py ) 


___


### PROJECT-12 GUESS THE NUMBER
```python

from random import randint
from art import logo

EASY_LEVEL_TURNS = 10
HARD_LEVEL_TURNS = 5

#Function to check user's guess against actual answer.
def check_answer(guess, answer, turns):
  """checks answer against guess. Returns the number of turns remaining."""
  if guess > answer:
    print("Too high.")
    return turns - 1
  elif guess < answer:
    print("Too low.")
    return turns - 1
  else:
    print(f"You got it! The answer was {answer}.")

#Make function to set difficulty.
def set_difficulty():
  level = input("Choose a difficulty. Type 'easy' or 'hard': ")
  if level == "easy":
    return EASY_LEVEL_TURNS
  else:
    return HARD_LEVEL_TURNS

def game():
  print(logo)
  #Choosing a random number between 1 and 100.
  print("Welcome to the Number Guessing Game!")
  print("I'm thinking of a number between 1 and 100.")
  answer = randint(1, 100)
  print(f"Pssst, the correct answer is {answer}") 

  turns = set_difficulty()
  #Repeat the guessing functionality if they get it wrong.
  guess = 0
  while guess != answer:
    print(f"You have {turns} attempts remaining to guess the number.")

    #Let the user guess a number.
    guess = int(input("Make a guess: "))

    #Track the number of turns and reduce by 1 if they get it wrong.
    turns = check_answer(guess, answer, turns)
    if turns == 0:
      print("You've run out of guesses, you lose.")
      return
    elif guess != answer:
      print("Guess again.")


game()

```

[Run this project]( https://replit.com/@Aristo00071/guess-the-number-start#main.py ) 



___



### PROJECT-14 HIGHER-LOWER

```python

from game_data import data
from art import logo,vs
import random
from replit import clear



def randm_account():
	return random.choice(data)


def format_descp(account_data):
	name=account_data['name']
	des=account_data['description']
	country=account_data['country']
	return f"{name}, a {des}, from {country}"


def check_winner(a ,b):
	if a>b:
		return 'a'
	else:
		return 'b'




def game():
	print(logo)


	game_cont=True
	score=0
	while(game_cont):
		first_ac=randm_account()
		sec_ac=randm_account()


		followerA=first_ac["follower_count"]
		followerB=sec_ac["follower_count"]


		formated_fst=format_descp(first_ac)
		formated_seec=format_descp(sec_ac)

		print(f"Compare A: {formated_fst}")
		print(vs)
		print(f"Against B: {formated_seec}")
		

		get_input=(input("Who has more followers? Type 'A' or 'B':")).lower()
		get_winner=check_winner(followerA,followerB)
		clear()
		print(logo)
		if get_input==get_winner:
			score+=1
			print(f"You're right! Current score: {score}.")
		else:
			print(f"Sorry, that's wrong. Final score: {score}")
			game_cont=False
		

game()

```
[Run this project]( https://replit.com/@Aristo00071/higher-lower-start#main.py ) 

___
