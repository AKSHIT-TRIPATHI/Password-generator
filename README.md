# Password-generator
random pass. generator.
import random
import array


f="yes"
print("**************WELCOME TO RANDOM PASSWORD GENERATOR***************")
while(f=="YES" or f=="yes"):
        print("_____PLESE ENTER VALUE MORE THAN 12_____")
        #taking input from the user
        
        MAX_LEN = int(input("How many charaters do you want as password ?"))
        #Checking the number is greater than or equal to required
        if MAX_LEN>=12:

                
                DIGITS = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
                LOCASE_CHARACTERS = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'm', 'n', 'o', 'p', 'q','r', 's', 't', 'u', 'v', 'w', 'x', 'y','z']
                UPCASE_CHARACTERS = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H','I', 'J', 'K', 'M', 'N', 'O', 'P', 'Q','R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y','Z']
                SYMBOLS = ['@', '#', '$', '%',':', '?','*']
                #combing the list to get the random values from a common list
                COMBINED_LIST = DIGITS + UPCASE_CHARACTERS + LOCASE_CHARACTERS + SYMBOLS

                
                rand_digit = random.choice(DIGITS)
                rand_upper = random.choice(UPCASE_CHARACTERS)
                rand_lower = random.choice(LOCASE_CHARACTERS)
                rand_symbol = random.choice(SYMBOLS)
                temp_pass = rand_digit + rand_upper + rand_lower + rand_symbol


                
                for x in range(MAX_LEN - 4):
                        temp_pass = temp_pass + random.choice(COMBINED_LIST)
                        temp_pass_list = array.array('u', temp_pass)
                        random.shuffle(temp_pass_list)

                
                password = ""
                for x in temp_pass_list:
                                password = password + x
                print("-------------------------------------------------------")
                print("Your Password is: ",password)
                print("--------------------------------------------------------")
        else:
                print("Invalid input ...PLEASE...try to input Agian..")
        f=input("I you want to generate the password again then write \"YES\" otherwise write \"NO\": ")
        if f=="Yes" or "yes":
                print()
                print()
                print()
                print()
print("__________________________________________________________________________________________")
      
print(".....................Thank You for visiting us.......................")
