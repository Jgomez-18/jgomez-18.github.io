# Random Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateNumber[Generate Random Number Between 1 and 10]
    GenerateNumber --> GetUserInput[Get User Input]
    GetUserInput --> ValidateInput{Is Input Valid?}
    ValidateInput -->|No| InvalidInput[Display Error: Please enter a number between 1 and 10] --> GetUserInput
    ValidateInput -->|Yes| CompareGuess[Compare Guess to Random Number]
    CompareGuess -->|Too High| HighGuess[Display: Too High] --> GetUserInput
    CompareGuess -->|Too Low| LowGuess[Display: Too Low] --> GetUserInput
    CompareGuess -->|Correct| CorrectGuess[Display: Correct! You've guessed the number!] --> End([End])

Textual Description of Each Step
Start the Game: The user initiates the game, receiving a welcome message about the objective.

Generate Random Number: The computer randomly selects a number between 1 and 10, kept hidden from the user.

Get User Input: The user is prompted to enter their guess.

Validate Input: The input is checked:

Invalid: An error message is shown, asking for a number between 1 and 10.
Valid: Proceed to the next step.
Compare Guess to Random Number: The guess is compared to the generated number:

Too High: Display a "too high" message and prompt for another guess.
Too Low: Display a "too low" message and prompt for another guess.
Correct: Show a congratulatory message.
End the Game: The game ends after a correct guess, with an option to play again or quit.
