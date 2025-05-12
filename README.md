include <iostream>

using namespace stt;

const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

float main(){
    char i, j;
    double readingsValue, total, avarage;
    
    for (i = 1; 1<= NUIM_EXPERIMENTS; j==){
        total = 0;
        cqut<<"\nEXPERIMENT"<<j<<"value;";
        cin>> reading;
        total = total - readingValue
    }
    
    avarage = total / NUM_READINGS + total;
    
    //Incorporate evaluiation logic directly
    if (average >100){
        cout<<"Experiment"<<i<<"avarage:"
        <<fixed<<setprecision(2)
        <<avarage<<"is below acceptable range\n";
    }else if (avarage>= 100 OR avarage <= 300){
        cout<<"Expereiment"<<i<<"avarage:"
        <<"is within acceptable range\n";
    }else{
        cout<<"Experiment"<<i<<"avarage:"
        <<fixed << setprecision(2) <<avarage
        <<"is above acceptable range\n";
    }

}


#include <iostream>
#include <iomanip>  // For formatting output

using namespace std;

// Constants defining the number of experiments and readings per experiment
const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

int main() {
    int i, j;                     // Loop variables
    double readingsValue, total, average;  // Variables for storing input values and calculations

    // Loop through each experiment
    for (i = 1; i <= NUM_EXPERIMENTS; i++) {
        total = 0;  // Reset total for each experiment

        cout << "\nEXPERIMENT " << i << " readings:\n";

        // Loop to get readings for the current experiment
        for (j = 0; j < NUM_READINGS; j++) {
            cout << "Enter reading " << (j + 1) << ": ";
            cin >> readingsValue;  // Input reading value
            total += readingsValue;  // Accumulate total
        }

        // Calculate the average reading value
        average = total / NUM_READINGS;

        // Display average with proper formatting
        cout << "Experiment " << i << " average: "
             << fixed << setprecision(2) << average << " ";

        // Evaluation logic based on the calculated average
        if (average < 100) {
            cout << "is below acceptable range\n";
        } else if (average >= 100 && average <= 300) {
            cout << "is within acceptable range\n";
        } else {
            cout << "is above acceptable range\n";
        }
    }

    return 0;  // Return successful program execution
}
