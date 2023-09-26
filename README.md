# Number-guessing-game-by-computer
import random as rn
print('Please Guess a Number From 0 to 100\n')
numbers = []
for i in range(101):
    numbers.append(i)
choose = []
while choose != 1:
    ebteda=numbers[0]
    enteha=numbers[-1]
    if len(numbers)>1: 
        ans = rn.randrange(ebteda,enteha)
        print('Your Guess Is '+str(ans))
        choose = int(input('\n1:The guess is correct\n2:the desired number is larger\n3:the desired number is smaller\n'))
        if choose == 3:
            del numbers[numbers.index(ans):-1]
            numbers.pop(-1)
                
        elif choose == 2:
            del numbers[0:numbers.index(ans)]
            numbers.pop(numbers.index(ans))
    else:
        print('Your Guess Is '+str(ans))
        break
