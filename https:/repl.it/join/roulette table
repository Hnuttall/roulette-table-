import random
cash = 10000
outcome = 0
beton = ""
cashout = "no"
cashoutnum = ""

#Show highscores
print("Welcome to the THB casino :)")
f = open('highscores.txt', 'r')
highscore = f.read()
print("\nThe current highscore is", highscore, "!")
f.close()

try:
  highscore = int(highscore)
except:
  highscore = 0

while cash > 0:
  print("for testing purposes just enter n\n\n")
  beton = input("Would you like to bet on numbers (36/1")

  if beton == "numbers" or beton == "n":
    print("Your cash stack: ", cash)
    num = random.randint(1,36)
    betnum = int(input("\n\nEnter the number you want to bet on, from 1-36(36/1): "))
    bet = int(input("enter the amount you want to bet: "))
    if betnum == num: 
      print("you bet on ", betnum, "the wheel rolled a ", num )
      cash = cash + bet*36
      print("Your cash stack: ", cash)
      print("would you like to cashout now and save your high score of ", cash, "?")
      cashout  = input()
    else:
      print("you bet on ", betnum, "the wheel rolled a ", num )
      print("you failed")
      cash = cash - bet
      print(cash)
      print("would you like to cashout now and save your high score of ", cash, "?")
      cashout  = input()  
         

  if cash == 0:
    print("Thanks for betting at The THB casino, come again :)")

  if cashout == "yes":
    cashoutnum = cash
    cash = 0 
    print("you cashed out for, £", cashoutnum, "enjoy!")
    if highscore < cashoutnum:
      f = open('highscores.txt', 'w+')
      f.write(str(cashoutnum))
      f.close()
    break

#if 5 % 2 == 0:
#  print("even")
