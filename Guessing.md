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
