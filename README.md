### Introduction:
To implement the tic tac toe game brings the classic pen-and-paper game to life in a digital format. Enjoy the simplicity and strategy of Xs and Os in this timeless and engaging gaming experience.

### Features:
1. Game Board:A 3x3 grid where players make their moves.
2.Player Turns:Alternating turns between Player X and Player O.
3.Move Validation:Ensure that player moves are valid and within the bounds of the game board.

### Requirements:
1.Front end: Python3
2.Back end: Python 3.6.0 interpreter
3.Jupyter Lab

### System flow diagram:
![pic1](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/5388dca5-ba6c-41c5-a86a-46fce560937a)
![pic2](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/1f1e2fcb-6fb3-45ad-b658-e9b5d7c33e62)


### Usage:
1.Entertainment:Tic Tac Toe is primarily played for fun and entertainment. It's a quick and engaging game that can be enjoyed by people of all ages.

2.Educational Tool:It helps develop critical thinking skills as players plan their moves to achieve victory or prevent their opponent from winning.

3.Teaching Programming:Implementing a Tic Tac Toe game is a popular project for beginners learning programming. It covers fundamental concepts such as control flow, data structures, and user input.

4.Problem-Solving Exercise:In educational settings, Tic Tac Toe can be used as a problem-solving exercise. Students can analyze and optimize the game's logic, exploring different algorithms for move selection.

5.Brain Training:Playing Tic Tac Toe involves strategic thinking and planning, making it a game that can contribute to brain training and cognitive development.

### Program:
```
board = ["-", "-", "-",
         "-", "-", "-",
         "-", "-", "-"]
 
# Define a function to print the game board
def print_board():
    print(board[0] + " | " + board[1] + " | " + board[2])
    print(board[3] + " | " + board[4] + " | " + board[5])
    print(board[6] + " | " + board[7] + " | " + board[8])
# Define a function to handle a player's turn
def take_turn(player):
    print(player + "'s turn.")
    position = input("Choose a position from 1-9: ")
    while position not in ["1", "2", "3", "4", "5", "6", "7", "8", "9"]:
        position = input("Invalid input. Choose a position from 1-9: ")
    position = int(position) - 1
    while board[position] != "-":
        position = int(input("Position already taken. Choose a different position: ")) - 1
    board[position] = player
    print_board()
# Define a function to check if the game is over
def check_game_over():
    # Check for a win
    if (board[0] == board[1] == board[2] != "-") or \
       (board[3] == board[4] == board[5] != "-") or \
       (board[6] == board[7] == board[8] != "-") or \
       (board[0] == board[3] == board[6] != "-") or \
       (board[1] == board[4] == board[7] != "-") or \
       (board[2] == board[5] == board[8] != "-") or \
       (board[0] == board[4] == board[8] != "-") or \
       (board[2] == board[4] == board[6] != "-"):
        return "win"
    # Check for a tie
    elif "-" not in board:
        return "tie"
    # Game is not over
    else:
        return "play"
 
# Define the main game loop
def play_game():
    print_board()
    current_player = "X"
    game_over = False
    while not game_over:
        take_turn(current_player)
        game_result = check_game_over()
        if game_result == "win":
            print(current_player + " wins!")
            game_over = True
        elif game_result == "tie":
            print("It's a tie!")
            game_over = True
        else:
            # Switch to the other player
            current_player = "O" if current_player == "X" else "X"
 
# Start the game
play_game()

```
### Output:
![g1](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/3be74843-7ac8-473c-b63f-6a71b81f0928)
![g2](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/c1623536-e367-4ddf-b01f-98bd0bbf0835)
![g3](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/59cf1208-37e8-436d-9721-598a992b6981)
![g4](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/9dee88e8-9a8e-4abf-9299-613040250232)
![g5](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/a6f1d837-4d27-4561-bb45-b5927b78ac00)
![g6](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/884d7644-b093-4d55-91f4-d10bdebafe6a)
![g7](https://github.com/Ritika-2706/Implementation-of-Tic-Tac-Toe/assets/93427238/06a1cbd8-eb55-4c96-8d99-cf9c339d7021)


### Result:
The player who succeeded in placing three respective marks in a horizontal, vertical, or diagonal row wins the game. The Tic Tac Toe is a great way to pass your free time whether you're standing in a line or spending time with your kids.
