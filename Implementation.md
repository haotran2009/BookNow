# Implementation Guide

## Phase 1

### Instructions for Running BookNow Application

#### 1. Switch to JavaFX 21 and Java 21 (if needed):
- Ensure you have **JavaFX 21** installed.
- Update to **Java 21** if required to ensure compatibility with the project environment.
- You might need to manually add javafx 21.0.4 lib if so download, will have to add VM options in edit configurations and fill out the necessary 

#### 2. Set Up MySQL Workbench:
- Download and install **MySQL-8.4.2**, and **MySQL Workbench**. 
- Use the following default settings for the database connection:
  - **User**: `root`
  - **Password**: `root`
  - **Database Name**: `booknow`

#### 3. Database Setup:
- Copy and paste the provided **DBScript** into MySQL Workbench and execute it.
- This script will create the necessary tables for the application to function correctly.

---

### Issues and Future Enhancements

- Any issues encountered during setup should be addressed. MacOS users may face errors that require manual troubleshooting, while the setup has been tested and works fine on Windows.
- If mac gives an error, related so mac internal when building then create a virtual windows machine or linux and run code from there. 
- Future updates will include an executable JAR file, eliminating the need for manually building the program. However, database setup will still be required.
- The feature called **Manual Restaurant Data Management** involves managing restaurant data using an SQL script. Once all related functionality—such as adding, updating, and 
retrieving restaurant information—has been fully implemented, this feature will be considered complete.

---

### Error Handling (Work in Progress)

- Several areas of the application still require better error handling. If you prefer strict error checks, note that this aspect is currently under development.
- Planned improvements for error handling will be implemented in the near future. For now, the focus is on testing the core functionality of the program: user creation, login, and restaurant search.

---

## Features Overview

### User Authentication

This feature enables users to create new accounts and log in to the system.

#### Implementation:
- Users can create an account with a unique username and password.
- Upon successful login with valid credentials, the user is directed to the main page.
- Basic error handling for incorrect credentials and duplicate usernames has been implemented.
- Further validation checks (e.g., password length) will be added soon.

#### Testing:
1. Create a new account by entering a unique username, a password, and confirming the password.
2. Log in using the valid credentials, which should take you to the **BookNow Dashboard**.
3. Attempt to log in with incorrect credentials to trigger an error message.
  - A logout button will be implemented soon to avoid restarting the program after each session.

---

### Search Restaurants

This feature enables users to search for restaurants based on criteria such as location, cuisine type, date, and number of guests.

#### Implementation:
- Users can filter restaurants by location, cuisine type, date, and number of guests (adults/children).
- Matching restaurants based on the selected filters will be fetched and displayed.

#### Testing:
1. Select a **location** and **cuisine type** from the dropdown menus.
2. Choose a **date**. Note that the selected date cannot be older than the current local date, and selecting an invalid date will trigger an error message.
3. Specify the **number of guests** (adults and children).
4. Click the "Search" button and verify that matching restaurants are displayed.

## Note
- You'll only see the Restaurant Name, location and a brief description. 
- Adding pictures, menus, reviews, etc will be implemented soon. 

---

### Upcoming Features

- **Restaurant Details & Reviews**: Features to display detailed restaurant information, images, and customer reviews will be implemented soon.
- **Max Number of Guests**: The dropdowns for selecting the number of adults and children are currently placeholders. These will be functional soon, with proper validation for guest selection.
- Additional features and improvements will follow in the next milestone.
