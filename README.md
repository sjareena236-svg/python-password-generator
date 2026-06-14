# python-password-generator
import random
import string
def generate_password():
  print("=== Random Password Generator ===")
  while True:
   try:
      len=int(input("Enter Password lenght:"))
      if len <4:
        print("length should be atleast 4")
        continue
      break
      except ValueError:
       print("please enter a number")
#get type preferences
use_letters=input("include letters?y/n:").lower()=='y'
use_numbers=input("include numbers?y/n:").lower()=='y'
use_symbols=input("include symbols?y/n:").lower()=='y'
#building character set
ch=""
if use_letters:
   ch+=string.ascii_letters
if use_numbers:
    ch+=string.digits
if use_symbols:
   ch+=string.puncuation
if not ch:
   print("you must select at least 1 character type!")
   return
password=".join(random.choice(ch)for_in range(length))
print(f"\n Generate Password:{password}")
if_name_=="_main_":
   generate_password()
   
