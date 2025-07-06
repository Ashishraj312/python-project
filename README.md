# python-project
#Project made using python language given by codsoft for internship
# project 1 - Password generator
import random
import string

def generate_password(length=12):
    if length < 4:
        print("Password length should be at least 4 characters.")
        return ""

    # Define character pools
    letters = string.ascii_letters
    digits = string.digits
    symbols = string.punctuation

    # Ensure at least one character from each type
    password = [
        random.choice(letters),
        random.choice(digits),
        random.choice(symbols)
    ]

    # Fill the rest of the password length
    all_chars = letters + digits + symbols
    password += random.choices(all_chars, k=length - 3)

    # Shuffle the result
    random.shuffle(password)

    return ''.join(password)

