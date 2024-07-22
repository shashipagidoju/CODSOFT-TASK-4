import random

def determine_winner(player_choice, computer_choice):
    if player_choice == computer_choice:
        return "It's a tie!"

    elif player_choice == 'rock':
        if computer_choice == 'paper':
            return 'Computer wins!'
        else:
            return 'Player wins!'

    elif player_choice == 'paper':
        if computer_choice == 'scissors':
            return 'Computer wins!'
        else:
            return 'Player wins!'

    elif player_choice == 'scissors':
        if computer_choice == 'rock':
            return 'Computer wins!'
        else:
            return 'Player wins!'

    else:
        return 'Invalid input! You have to choose rock, paper, or scissors.'

def main():
    choices = ['rock', 'paper', 'scissors']

    while True:
        print("\nLet's play Rock, Paper, Scissors!")
        print("Enter your choice: rock, paper, scissors")
        player_choice = input("Your choice: ").lower()

        if player_choice not in choices:
            print("Invalid input! Please enter either rock, paper, or scissors.")
            continue

        computer_choice = random.choice(choices)
        print(f"Computer chose: {computer_choice}")

        result = determine_winner(player_choice, computer_choice)
        print(result)

        play_again = input("Do you want to play again? (yes/no): ").lower()
        if play_again != 'yes':
            print("Thanks for playing!")
            break

if __name__ == "__main__":
    main()

