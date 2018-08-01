# NumberGuess
Wanna play a game? In this project, we'll build a program that rolls a pair of dice and asks the user to guess the sum. If the user's guess is equal to the total value of the dice roll, the user wins! Otherwise, the computer wins. 

    from random import randint
    from time import sleep

    def get_user_guess():
      guess = int(raw_input("Guess a number: "))
      return guess

    def roll_dice(number_of_sides):

      first_roll = randint(1,number_of_sides)
      second_roll = randint(1,number_of_sides)

      max_val = number_of_sides * 2
      print "The maximum value these dices together can hold is %d " % (max_val)

      guess = get_user_guess()

      if guess > max_val:
        print  "No guessing higher than the maximum possible value!"

      else:
          print "Rolling..."
          sleep(2)
          print "The first roll came up to %d" % (first_roll)
          sleep(1)
          print "The second roll came up to %d" % (second_roll)
          sleep(1)
          total_roll = first_roll + second_roll
          print "Result..."
          sleep(1)

          if guess == total_roll:
              print "Congratulations!, you guessed it right."
          else:
              print "You lost, try again"




    roll_dice(6)  
