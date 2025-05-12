#include <iostream>
#include <iomanip>

using namespace std;

const int NUM_EXPERIMENTS = 3;
const int NUM_READINGS = 3;

float main() {
    double readingsValue, total, average;

    for (int i = 1; i <= NUM_EXPERIMENTS; i++) {  // Corrected loop condition
        total = 0;
        cout << "\nEXPERIMENT " << i << " values:\n";
        cout<<""==================\n";

        for (int j = 1; j <= NUM_READINGS; j++) {  // Fixed inner loop syntax
            cout << "Reading " << j << ": ";
            cin >> readingsValue;
            total += readingsValue;  // Corrected total calculation
        }

        average = total / NUM_READINGS;  // Corrected average calculation

        // Evaluation logic
        cout << "Experiment " << i << " average: " << fixed << setprecision(2) << average << " ";

        if (average < 100) {
            cout << "is below acceptable range.\n";
        } else if (average >= 100 && average <= 300) {  // Fixed logical OR syntax
            cout << "is within acceptable range.\n";
        } else {
            cout << "is above acceptable range.\n";
        }
    }

    return 0;
}
