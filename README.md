#include <iostream>
#include <string.h>

using namespace std;

//Global variables
string POKEMON_1 = "Charizard";
string POKEMON_2 = "Pikachu";

//Pokemon HP
int hp1 = 60;
int hp2 = 65;



//Function Prototypes
void displayHPBar(int);
void displayCharizardSkills();
void displayPikachuSkills();

int main(){
    cout<<POKEMON_1<<":";
    displayHPBar(hp1);
    cout<<POKEMON_2<<":";
    displayHPBar(hp2);
    
    displayCharizardSkills();
    
    int choice;
    cout<<"Enter Skill Number:";
    cin>>choice;
    
    return 0;
}

void displayCharizardSkills(){
    string CharizardSkills[] = {"Flamethrower","Air Slash","Fire Spin","Dragon Claw"};
    int lenght = sizeof(CharizardSkills) / sizeof(CharizardSkills[0]);
    
    for(int x=0;x<lenght;x++){
        cout<<x+1<<"."<<CharizardSkills[x]<<endl;
    }
}

//Function Definitions
void displayHPBar(int hp){
    
    for(int x=hp;x>0;x-=5){
        cout << "|";
    }
    cout<<hp<<endl;
}







