# Random Guessing Game Flowchart

```mermaid
flowchart TD
    A[Start] --> B[Generate random number between Min and Max]
    B --> C[Display instructions to the user]
    C --> D[Get user guess]
    D --> E{Is input numeric?}
    E -- Yes --> F{Is guess within range?}
    E -- No --> G[Display "Please enter a valid number"]
    G --> D

    F -- Yes --> H{Is guess equal to random number?}
    F -- No --> I[Display "Please guess a number within the range"]
    I --> D

    H -- Yes --> J[Display "Congratulations! You guessed it right!"]
    H -- No --> K{Is guess too high?}
    
    K -- Yes --> L[Display "Your guess is too high. Try again."]
    K -- No --> M[Display "Your guess is too low. Try again."]
    
    L --> D
    M --> D

    J --> N[End]
