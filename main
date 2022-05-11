import Game_Files
import random

def person_a():
    '''summons a random dictionary, then returns that dictionary'''
    data_a = Game_Files.data[random.randint(0,50)]
    # print(data_a)
    return data_a
def person_b():
    '''summons a second random dictionary, then returns that dictionary'''
    data_b = Game_Files.data[random.randint(0,50)]
    # print(data_b)
    while PERSON_A == data_b:
        data_b = Game_Files.data[random.randint(0,50)]
    return data_b
def comparison(a, b):
    '''compares the follower count between a and b, then returns the dictionary of the highest count'''
    if a > b:
        return PERSON_A
    elif b > a:
        return PERSON_B


game_lost = False
score = 0
repeat = False
#Constants listed in capitals
PERSON_A = person_a()
DATA_A = PERSON_A['follower_count']


print("Welcome to the Higher/Lower Game\nGuess which celebrity has more followers on instagram and compete for a highscore!\nGood luck!")
while not game_lost:
    if repeat == True:
        PERSON_A = result
        DATA_A = result['follower_count']

    PERSON_B = person_b()
    DATA_B = PERSON_B['follower_count']

    result = comparison(a=DATA_A, b=DATA_B)
    # print(result) //debugging code//


    print(f"\nPerson 'A' is {PERSON_A['name']}: a {PERSON_A['description']} from {PERSON_A['country']}")
    print(f"\nPerson 'B' is {PERSON_B['name']}: a {PERSON_B['description']} from {PERSON_B['country']}")

    guess = input("\nGuess A or B: ").lower()
    if guess == 'a':
        if DATA_A == result['follower_count']:
            score += 1
            repeat = True
        elif DATA_A != result['follower_count']:
            print(f"Sorry, the correct answer is {result['name']}.")
            game_lost = True
    if guess == 'b':
        if DATA_B == result['follower_count']:
            score += 1
            repeat = True
        elif DATA_B != result['follower_count']:
            print(f"Sorry, the correct answer is {result['name']}.")
            game_lost = True

print(f"Your final score is {score}")
