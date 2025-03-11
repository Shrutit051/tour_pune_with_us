# Travel Preferences and Destination Recommendation System

## Overview

The **Travel Preferences and Destination Recommendation System** is a Java-based application that allows users to input their travel preferences and receive personalized destination recommendations. The system uses a MySQL database to store user information, preferences, and destination details. It provides both a **command-line interface (CLI)** and a **graphical user interface (GUI)** for user interaction.

## Video link
https://drive.google.com/file/d/1kwlwRwPUqTs-vJDM8iP3DSx8RLyjOeMh/view?usp=sharing

## Features

### User Features
1. **Input User Details**: Users can input their name, contact, and email.
2. **Select Travel Preferences**:
   - **Transport Preference**: Choose from available transportation options.
   - **Hotel Preference**: Select from available hotel types.
   - **Destination Type**: Choose the type of destination (e.g., beach, mountain, city).
   - **Travel Month**: Select the preferred month for travel.
   - **Budget**: Enter the travel budget.
3. **Destination Recommendation**: Based on the user's preferences, the system recommends a suitable destination with details such as description, minimum cost, transport cost, and hotel cost.

### Database Integration
- **User Table**: Stores user details (name, contact, email).
- **Preferences Table**: Stores user preferences (transport, hotel, destination type, travel month, budget).
- **Destinations Table**: Stores destination details (name, description, minimum cost, suitable months).
- **Transportation Table**: Stores transportation options and costs.
- **Hotels Table**: Stores hotel types and prices.

## Technologies Used

- **Java**: Core programming language.
- **MySQL**: Database management system.
- **JDBC**: Java Database Connectivity for interacting with the MySQL database.
- **Swing**: For building the graphical user interface (GUI).

## Code Structure

### Main.java (CLI Version)
- **Purpose**: Command-line interface for collecting user details and preferences.
- **Key Features**:
  - Collects user details and inserts them into the `user` table.
  - Displays available options for transport, hotel, destination type, and travel month.
  - Collects user preferences and inserts them into the `preferences` table.

### MainUI.java (GUI Version)
- **Purpose**: Graphical user interface for collecting user details and preferences.
- **Key Features**:
  - Provides a user-friendly form for inputting user details and preferences.
  - Populates dropdowns with data from the database.
  - Inserts user data and preferences into the database.
  - Recommends a destination based on user preferences.

## How to Run the Code

### Prerequisites
1. **MySQL Database**:
   - Ensure MySQL is installed and running.
   - Create a database named `dbmsminipro`.
   - Import the provided SQL schema to create the necessary tables (`user`, `preferences`, `destinations`, `transportation`, `hotels`).

2. **Java Development Kit (JDK)**:
   - Ensure JDK is installed on your system.

3. **MySQL Connector/J**:
   - Download the MySQL Connector/J driver and add it to your project's classpath.

### Steps to Run

#### CLI Version (Main.java)
1. **Compile the Java Code**:
   ```bash
   javac dbmsminipro/Main.java
   ```

2. **Run the Application**:
   ```bash
   java dbmsminipro.Main
   ```

3. **Follow the On-Screen Instructions**:
   - Enter your details (name, contact, email).
   - Select your travel preferences from the displayed options.
   - Enter your budget.
   - The system will insert your data into the database.

#### GUI Version (MainUI.java)
1. **Compile the Java Code**:
   ```bash
   javac dbmsminipro/MainUI.java
   ```

2. **Run the Application**:
   ```bash
   java dbmsminipro.MainUI
   ```

3. **Use the GUI**:
   - Fill in the form with your details and preferences.
   - Click the "Submit" button to save your data and receive a destination recommendation.

## Example Usage

### CLI Version
1. **Enter User Details**:
   ```
   Enter your name: John Doe
   Enter your contact: 1234567890
   Enter your email: john.doe@example.com
   ```

2. **Select Preferences**:
   ```
   Available transport preferences:
    - Bus
    - Train
    - Flight
   Enter your transport preference: Flight

   Available hotel preferences:
    - Budget
    - Luxury
   Enter your hotel preference: Luxury

   Available destination types:
    - Beach
    - Mountain
    - City
   Enter your destination type: Beach

   Available travel months:
    - January
    - February
    - March
   Enter your travel month: January

   Enter your budget: 5000
   ```

3. **Output**:
   ```
   User added successfully with ID: 1
   Preferences added successfully!
   ```

### GUI Version
1. **Fill in the Form**:
   - Name: John Doe
   - Contact: 1234567890
   - Email: john.doe@example.com
   - Budget: 5000
   - Transport Preference: Flight
   - Hotel Preference: Luxury
   - Destination Type: Beach
   - Travel Month: January

2. **Click "Submit"**:
   - A message box will display the recommended destination and its details.

## Database Schema

### Tables
1. **user**:
   - `user_id` (Primary Key)
   - `name`
   - `contact`
   - `email`

2. **preferences**:
   - `preference_id` (Primary Key)
   - `user_id` (Foreign Key)
   - `budget`
   - `transport_preference`
   - `hotel_preference`
   - `destination_type`
   - `travel_month`

3. **destinations**:
   - `destination_id` (Primary Key)
   - `name`
   - `description`
   - `type`
   - `min_cost`
   - `suitable_months`

4. **transportation**:
   - `transport_id` (Primary Key)
   - `type`
   - `cost_per_km`

5. **hotels**:
   - `hotel_id` (Primary Key)
   - `hotel_type`
   - `destination_id` (Foreign Key)
   - `price_per_night`

## Future Enhancements

1. **User Authentication**: Implement a login system for users.
2. **Advanced Recommendations**: Use machine learning algorithms for more personalized recommendations.
3. **Payment Integration**: Allow users to book and pay for their travel directly through the application.
4. **Multi-Language Support**: Add support for multiple languages.
5. **Admin Panel**: Create an admin panel to manage destinations, transportation, and hotels.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Java Swing**: For providing the GUI framework.
- **MySQL**: For the database management system.
- **JDBC**: For enabling database connectivity in Java.

##Team members
- Sanika Shidore (UCE2023461)
- Shreya Gujarathi (UCE2023463)
- Siddhi Vaidya (UCE2023464)
- Shruti Thakur (UCE2023469)
- This is our Mini Project for our course Database Management Systems Laboratory (Course code - 23PCCE301L) of semester 3, second year, computer engineering!

---

This README provides a comprehensive overview of the Travel Preferences and Destination Recommendation System, including its features, technologies, code structure, and instructions on how to run the code. It also outlines potential future enhancements and acknowledges the technologies used.
