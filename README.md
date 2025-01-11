#include <iostream>
#include <vector>
#include <string> // Include necessary headers

// Structure to represent a car
struct Car {
    std::string model;
    std::string make;
    int year;
    double dailyRate;
    bool available; // Track availability
};

// Structure to represent a rental
struct Rental {
    int rentalId;
    std::string customerName;
    Car rentedCar;
    int daysRented;
    double totalCost;
};


// Function prototypes (you'll need to implement these)
void addCar(std::vector<Car>& cars, const Car& newCar);
void rentCar(std::vector<Car>& cars, std::vector<Rental>& rentals, const std::string& customerName, const std::string& carModel, int days);
void returnCar(std::vector<Rental>& rentals, int rentalId);
void displayAvailableCars(const std::vector<Car>& cars);
void displayRentals(const std::vector<Rental>& rentals);


int main() {
    std::vector<Car> cars;
    std::vector<Rental> rentals;

    // Example cars (you would typically load these from a database)
    addCar(cars, {"Toyota Camry", "Toyota", 2023, 50.0, true});
    addCar(cars, {"Honda Civic", "Honda", 2022, 45.0, true});

    // ... (Main menu loop with user interaction) ...

    int choice;
    do {
        // Display menu options
        std::cout << "1. Add Car\n";
        std::cout << "2. Rent Car\n";
        std::cout << "3. Return Car\n";
        std::cout << "4. Display Available Cars\n";
        std::cout << "5. Display Rentals\n";
        std::cout << "0. Exit\n";
        std::cout << "Enter your choice: ";
        std::cin >> choice;

        switch (choice) {
            case 1: // addCar()
                break;
            case 2: // rentCar()
                break;
            case 3: // returnCar()
                break;
            case 4: // displayAvailableCars()
                break;
            case 5: // displayRentals()
                break;
            case 0:
                std::cout << "Exiting...\n";
                break;
            default:
                std::cout << "Invalid choice!\n";
        }
    } while (choice != 0);

    return 0;
}


// Example function implementation (addCar)
void addCar(std::vector<Car>& cars, const Car& newCar) {
    cars.push_back(newCar);
    std::cout << "Car added successfully!\n";
}
