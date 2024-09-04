# githubbus
This is a short program that i wrote for my exam for programming 1.

This code is saved on my local computer

# Bastu 2.0

import random

# Fahrenheit till Celsius omvandling
def fahr_to_cel(fahrenheit):
    celsius = (fahrenheit - 32) * 5 / 9
    return celsius

# Slumpmässig Fahrenheit till Celsius omvandling
def fahr_to_cel_random():
    fahrenheit = random.randint(1, 100)
    return fahr_to_cel(fahrenheit)

# Huvudfunktion för temperaturkontroll i bastun
def main():
    celsius = 0
    while celsius < 82 or celsius > 87:
        try:
            user_input = input("Ange temperaturen i Fahrenheit (0 för att slumpa): ")
            if user_input == '0':
                celsius = fahr_to_cel_random()
            else:
                fahrenheit = int(user_input)
                celsius = fahr_to_cel(fahrenheit)

            if celsius < 82:
                print("Det är för kallt.")
            elif celsius > 87:
                print("Det är för varmt.")
            else:
                print("Temperaturen är lagom för bastun. Det är", celsius, "grader Celsius. Bastun är redo att bada i!")
        except ValueError:
            print("Felaktig inmatning. Var god ange ett heltal för Fahrenheit.")

# Kör huvudfunktionen om programmet körs direkt
if __name__ == "__main__":
    main()


