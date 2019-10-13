#include<iostream>
#include<ctime>
void PrintIntroduction(int Difficulty)
{
    std::cout << "\n\n You are a secret agent breaking into a level "<<Difficulty;
    std::cout << " secure server room ....\nEnter the correct code to continue...\n\n";
}
bool PlayGame(int Difficulty)
{
    PrintIntroduction(Difficulty);
    const int CodeA = rand() % Difficulty + Difficulty;
    const int CodeB = rand() % Difficulty + Difficulty;
    const int CodeC = rand() % Difficulty + Difficulty;
    
    const int CodeSum = CodeA + CodeB + CodeC;
    const int CodeProduct = CodeA * CodeB * CodeC;
    std::cout << "+There are 3 numbers in the code";
    std::cout << "\n+The codes add-up to: " << CodeSum;
    std::cout << "\n+The codes multiply to give : " << CodeProduct << std::endl;

    int GuessA , GuessB , GuessC;
    std::cin >> GuessA >> GuessB >> GuessC;

    int GuessSum = GuessA + GuessB + GuessC;
    int GuessProduct = GuessA * GuessB * GuessC ;

    if (GuessSum == CodeSum && GuessProduct == CodeProduct)
    {
        std::cout << "\n***Well done agent! You have extracted the file! keep going!***";
        return true;
    }
    else
    {
        std::cout << "\n***You entered the incorrect code! Careful agent! Try again***";
        return false;
    }
}

int main()
{
    srand(time(NULL));  // creates new random sequence based on time of  day

    int LevelDificulty = 1;
    int const MaxDifficulty = 5;

    while(LevelDificulty <= MaxDifficulty) //loop game until all levels completed
    {
        bool bLevelComplete = PlayGame(LevelDificulty);
        std::cin.clear();//clears any errors
        std::cin.ignore();//Discards Buffer
        if (bLevelComplete)
        {
            ++LevelDificulty;
        }
        
    }
    std::cout << "\n***Great work agent! You got all the files! Now get out of there! ***\n";
    return 0;
}
