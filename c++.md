## C++

# Constructor and Destructor


Constructor

*Automatic Initialiazation
*Reduced Code Duplication
*Ensures Proper Initialization
*Supports Parameterization
*Encapsulation of initialization logic

```bash
#include <iostream>
using namespace std;

class Person {
    string name;
    int age;
    string country;

public:
    // Default Constructor
    Person() {
        name = "Unknown";
        age = 0;
        country = "Not Specified";
        cout << "Default Constructor Called!" << endl;
    }

    // Parameterized Constructor
    Person(string n, int a, string c) {
        name = n;
        age = a;
        country = c;
        cout << "Parameterized Constructor Called!" << endl;
    }

    // Constructor using Initialization List
    Person(string n, int a) : name(n), age(a), country("Unknown") {
        cout << "Constructor with Initialization List Called!" << endl;
    }

    // Method to display details
    void display() {
        cout << "Name: " << name << ", Age: " << age << ", Country: " << country << endl;
    }
};

int main() {
    cout << "Creating person1 using Default Constructor:" << endl;
    Person person1; // Default Constructor

    cout << "\nCreating person2 using Parameterized Constructor:" << endl;
    Person person2("Alice", 30, "USA"); // Parameterized Constructor

    cout << "\nCreating person3 using Constructor with Initialization List:" << endl;
    Person person3("Bob", 25); // Constructor with Initialization List

    cout << "\nDisplaying details of all persons:" << endl;
    person1.display();
    person2.display();
    person3.display();

    return 0;
}


```
