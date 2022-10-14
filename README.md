import random
print('This is the rock, paper, scissors game thats played between two people. This game will be played between yourself and the computer.')
print()

print('start')
print()

def play():
    user = input("whats your choice? 'rock' for rock, 'paper' for paper, 'scissors' for scissors> ")
    user = user.lower()
    
    computer = random.choice(['rock', 'paper', 'scissors'])
    
    if user == computer:
        return "you and the computer have both chosen {}. ITS A TIE".format(computer)
    #rock > scissors, scissors > paper, paper > rock 
    if is_win(user, computer):
        return"you have chosen {} and the computer has chosen {}. YOU WIN!".format(user, computer)
    
    return "you have chosen {} and the computer has chosen {}. COMPUTER WINS!".format(user, computer)
    
def is_win(player, opponent):
    # return true is the player beats the opponent
    # winning conditions: rock > scissors, scissors > paper, paper > rock
    if (player == 'rock' and opponent == 'scissors') or (player == 'scissors' and opponent == 'paper') or (player == 'paper' and opponent == 'rock'):
            return True
    return False

if __name__== '__main__':
    print(play())
                            
                         
