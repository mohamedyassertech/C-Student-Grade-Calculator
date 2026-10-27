# C++ Student Grade Calculator

This is a beginner-level C++ console application developed as a first programming assignment. The program takes a student's name and three course grades, verifies that all grades are between 0 and 100, calculates the final average, and assigns an academic letter grade (A-F).

---

## 🔍 How the Code Works

1. **Variable Declarations:**  
   The program starts by creating a `string` variable (`name`) to store the student's name and four `double` variables (`grade1`, `grade2`, `grade3`, `average`) to hold decimal values for course scores and calculations.

2. **User Input:**  
   - `getline(cin, name)` reads the full student name, including any spaces.  
   - `cin >> grade1 >> grade2 >> grade3` captures the three numerical scores entered by the user.

3. **Input Validation (`if` Statement):**  
   Using logical OR operators (`||`), the code checks if any of the three grades are less than `0` or greater than `100`. If any score is out of range, the program prints `"INVALID Score"` and skips the rest of the calculations.

4. **Average Calculation & Formatting:**  
   If all grades are valid, the `else` block executes. It calculates the arithmetic mean using `(grade1 + grade2 + grade3) / 3` and assigns it to `average`, then displays the student's name and calculated average.

5. **Letter Grade Evaluation (`if-else` Chain):**  
   An `if-else` decision chain evaluates `average` against standard grading boundaries to display the final letter grade:
   - `average >= 90` ➔ **Grade is A**
   - `average >= 80` ➔ **Grade is B**
   - `average >= 70` ➔ **Grade is C**
   - `average >= 60` ➔ **Grade is D**
   - Otherwise ➔ **Grade is F**
     
<img width="1833" height="928" alt="Assignment 2" src="https://github.com/user-attachments/assets/bd814944-22f6-4149-a70e-86eff5566edf" />



https://github.com/user-attachments/assets/32a8f361-7b85-48a0-b365-a42e49eba579


---

## 💻 Source Code (`assignment.cpp`)

```cpp
#include <iostream>
#include <string>
using namespace std;

int main () {
    string name;
    double grade1;
    double grade2;
    double grade3;
    double average;

    cout << "Enter your name: ";
    getline (cin, name);

    cout << "Enter first grade: ";
    cin >> grade1;
    cout << "Enter second grade: ";
    cin >> grade2;
    cout << "Enter third grade: ";
    cin >> grade3;

    if (grade1 < 0 || grade1 > 100 || grade2 < 0 || grade2 > 100 || grade3 < 0 || grade3 > 100) {
        cout << "INVALID Score" << endl;
    }
    else {
        average = (grade1 + grade2 + grade3) / 3;
        cout << "Results" << endl;
        cout << "Name: " << name << endl;
        cout << "Final average: " << average << endl;
        
        if (average >= 90) {
            cout << "Grade is A" << endl;
        }
        else if (average >= 80) {
            cout << "Grade is B" << endl;
        }
        else if (average >= 70) {
            cout << "Grade is C" << endl;
        }
        else if (average >= 60) {
            cout << "Grade is D" << endl;
        }
        else {
            cout << "Grade is F" << endl;
        }
    }

    return 0;
}
