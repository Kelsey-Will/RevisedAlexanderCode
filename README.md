# RevisedAlexanderCode
#include <iostream>
#include <string>
using namespace std;

// Class representing a player
class Player {
public:
    string name;
    int level;

    void showStatus() {
        cout << "Player: " << name << " | Level: " << level << endl;
    }
};

// Class representing a quest
class Quest {
public:
    string title;
    int difficulty;

    // Pass Player by reference to update original level
    void completeQuest(Player& p) {
        cout << p.name << " has completed the quest '" << title << "'!" << endl;
        p.level += difficulty;
    }
};

int main() {
    Player hero;
    hero.name = "Ragnar";
    hero.level = 1;

    Quest quest1;
    quest1.title = "Defeat the Dragon";
    quest1.difficulty = 5;

    quest1.completeQuest(hero);
    hero.showStatus();  // Corrected function name

    return 0;
}
