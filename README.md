import time

def space():
    for rep in range(2):
        print("")

print("-" * 40)
print("             \033[4:34mCALCULATOR\033[m")
print("-" * 40)
print()
reply = "S"

while reply == "S" or "s":
    print("""         \033[7:36m[1] SUM           \033[m
         \033[7:36m[2] SUBTRACTION   \033[m
         \033[7:36m[3] MULTIPLICATION\033[m
         \033[7:36m[4] DIVISION      \033[m
         \033[7:36m[5] TABLES        \033[m""")
    print()

    try:
        choice = int(input("\033[1:32m What kind of calculation do you want? \033[m"))

        if choice == 1:
            print("")
            n1 = int(input("Enter a number: "))
            n2 = int(input("Enter another number: "))
            sum = n1 + n2
            space()

            process = "P", "R", "O", "C", "E", "S", "S", "I", "N", "G", ".", ".", "."

            for loading in process:
                print(f'\033[1:32m{loading}\033[m', end=" ", flush=True)
                time.sleep(0.5)

            space()
            print(f'\033[7:34m{n1} + {n2} = {sum}\033[m')
            print("")
            reply = str(input("\033[1:32mDo you wish to continue?\033[m ")).strip().upper()
            print("")

            if reply == "N":
                break

            elif reply != "S" or "N":
                print("\033[1:31m Could not understand your answer \033[m")
                print("")

        elif choice == 2:
            print("")
            n1 = int(input("Enter a number: "))
            n2 = int(input("Enter another number: "))
            subtraction = n1 - n2
            space()

            process = "P", "R", "O", "C", "E", "S", "S", "I", "N", "G", ".", ".", "."

            for loading in process:
                print(f'\033[1:32m{loading}\033[m', end=" ", flush=True)
                time.sleep(0.5)

            space()
            print(f'\033[7:34m{n1} - {n2} = {subtraction}\033[m')
            print("")
            reply = str(input("\033[1:32mDo you wish to continue?\033[m ")).strip().upper()
            print("")

            if reply == "N":
                break

            elif reply != "S" or "N":
                print("\033[1:31m Could not understand your answer \033[m")
                print("")

        elif choice == 3:
            space()
            n1 = int(input("Enter a number: "))
            n2 = int(input("Enter another number: "))
            multiplication = n1 * n2
            space()

            process = "P", "R", "O", "C", "E", "S", "S", "I", "N", "G", ".", ".", "."

            for loading in process:
                print(f'\033[1:32m{loading}\033[m', end=" ", flush=True)
                time.sleep(0.5)

            space()
            print(f'\033[7:34m{n1} X {n2} = {multiplication}\033[m')
            print("")
            reply = str(input("\033[1:32mDo you wish to continue?\033[m ")).strip().upper()
            print("")

            if reply == "N":
                break

            elif reply != "S" or "N":
                print("\033[1:31m Could not understand your answer \033[m")
                print("")

        elif choice == 4:
            space()
            n1 = int(input("Enter a number: "))
            n2 = int(input("Enter another number: "))
            division = n1 / n2
            space()

            process = "P", "R", "O", "C", "E", "S", "S", "I", "N", "G", ".", ".", "."

            for loading in process:
                print(f'\033[1:32m{loading}\033[m', end=" ", flush=True)
                time.sleep(0.5)

            space()
            print(f'\033[7:34m{n1} / {n2} = {division}\033[m')
            print("")
            reply = str(input("\033[1:32mDo you wish to continue?\033[m ")).strip().upper()
            print("")

            if reply == "N":
                break

            elif reply != "S" or "N":
                print("\033[1:31m Could not understand your answer \033[m")
                print("")

        elif choice == 5:
            print("")
            n1 = int(input("Enter a number: "))
            space()

            process = "P", "R", "O", "C", "E", "S", "S", "I", "N", "G", ".", ".", "."

            for loading in process:
                print(f'\033[1:32m{loading}\033[m', end=" ", flush=True)
                time.sleep(0.5)

            space()

            for count in range(1, 11, 1):
                tables = n1 * count
                print(f'\033[7:34m{n1} X {count} = {tables}\033[m')
            print("")
            reply = str(input("\033[1:32mDo you wish to continue?\033[m ")).strip().upper()
            print("")

            if reply == "N":
                break

            elif reply != "S" or "N":
                print("\033[1:31m Could not understand your answer \033[m")
                print("")

        else:
            print("")
            print("\033[1:31m Could not understand your answer \033[m")
            print("")

    except ValueError as choice:
        print("")
        print("       \033[4:31mERROR! Invalid Command\033[m")
        print("")
        break

if reply == "N":
    print("\033[7:31m Calculator closed \033[m")

