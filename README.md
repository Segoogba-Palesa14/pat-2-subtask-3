#include <iostream>
#include <iomanip>  // Include library for formatted output

using namespace std;

const int NUM_EXPERIMENTS = 3; // Define the number of experiments to conduct
const int NUM_READINGS = 3;  // Define the number of readings per experiment

int main() {
    double readingsValue, total, average;  // Variables for input readings, sum, and average

    // Loop through each experiment
    for (int i = 1; i <= NUM_EXPERIMENTS; i++) {  
        total = 0;  // Reset total for each experiment
        cout << "\nEXPERIMENT " << i << endl;  // Display experiment number
        cout << "==============\n";  // Display separator for clarity

        // Loop through each reading within an experiment
        for (int j = 1; j <= NUM_READINGS; j++) {  
            cout << "Enter reading " << j << " value: ";  // Prompt for reading input
            cin >> readingsValue;  // Take user input
            total += readingsValue;  // Accumulate readings for total sum
        }

        average = total / NUM_READINGS;  // Compute the average of readings

        // Display experiment average value with two decimal precision
        cout << "Experiment " << i << " average: " << fixed << setprecision(2) << average << " ";

        // Evaluate and classify the average value
        if (average < 100) {
            cout << "is below acceptable range.\n";
        } else if (average >= 100 && average <= 300) {  
            cout << "is within acceptable range.\n";
        } else {
            cout << "is above acceptable range.\n";
        }
    }

    return 0;  // Indicate successful program termination
}
