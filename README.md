# Password-maker
import random

def passwordMaker():
    password = ''

    for x in range(numbers):
        password += random.choice(chars)
    
    return password
    
try: 
    numbers = int(input('How many characters do you want your password? '))
    uppers = input('Do you want uppercase letters in your password (yes/no): ')
    special = input('Do you want special characters/numbers in your (yes/no): ')

    if uppers.lower().strip() == 'yes' :
       if special.lower().strip() == 'yes':
          chars = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#$%^&*(),.'
       elif special.lower().strip() == 'no':
           chars = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'
        
    elif uppers.lower().strip() == 'no' :
       if special.lower().strip() == 'yes':
           chars = 'abcdefghijklmnopqrstuvwxyz1234567890!@#$%^&*(),.'
       elif special.lower().strip() == 'no':
           chars = 'abcdefghijklmnopqrstuvwxyz'

    password = passwordMaker()

    print('Your password is: ')
    print(password)


except:
        print('Please input a number of characters.')
