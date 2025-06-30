# python-project
#Project made using python language given by codsoft for internship
# project 1 - OTP generator
import random

def generate_numeric_otp(length=6):
    otp = ''.join([str(random.randint(0, 9)) for _ in range(length)])
    return otp


print("Your OTP is:", generate_numeric_otp())
