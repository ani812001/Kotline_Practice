import kotlin.random.Random

fun main() {
    val choices = listOf("Rock", "Paper", "Scissors")
    
    // Function to get the user's choice
    fun getUserChoice(): String {
        println("Enter your choice (Rock, Paper, or Scissors):")
        var userChoice = readLine()?.capitalize()
        
        while (userChoice !in choices) {
            println("Invalid choice. Please enter Rock, Paper, or Scissors:")
            userChoice = readLine()?.capitalize()
        }
        return userChoice!!
    }

    // Function to get the computer's choice
    fun getComputerChoice(): String {
        return choices[Random.nextInt(choices.size)]
    }

    // Function to determine the winner
    fun determineWinner(userChoice: String, computerChoice: String) {
        println("You chose: $userChoice")
        println("Computer chose: $computerChoice")
        
        if (userChoice == computerChoice) {
            println("It's a tie!")
        } else if ((userChoice == "Rock" && computerChoice == "Scissors") ||
                   (userChoice == "Paper" && computerChoice == "Rock") ||
                   (userChoice == "Scissors" && computerChoice == "Paper")) {
            println("You win!")
        } else {
            println("Computer wins!")
        }
    }

    // Main game loop
    val userChoice = getUserChoice()
    val computerChoice = getComputerChoice()
    determineWinner(userChoice, computerChoice)
}

