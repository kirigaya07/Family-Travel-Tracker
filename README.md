# Family Travel Tracker

Family Travel Tracker is a web application built with Express.js and PostgreSQL that allows families to track the countries they have visited. Users can add new countries they have visited, view their visited countries, and switch between different family members.

## Features

- **User Management**: Family members can be added and switched between.
- **Country Tracking**: Users can add countries they have visited to their profile.
- **Error Handling**: Comprehensive error handling for invalid input and duplicate country entries.

## Technologies Used

- **Express.js**: Web application framework for Node.js used to handle HTTP requests.
- **PostgreSQL**: Open-source relational database management system.
- **body-parser**: Node.js middleware for parsing incoming request bodies.
- **ejs**: Embedded JavaScript templating for rendering dynamic content.

## Setup

1. Clone the repository: `git clone https://github.com/your-username/family-travel-tracker.git`
2. Install dependencies: `npm install`
3. Set up PostgreSQL database:
   - Create a PostgreSQL database named `Skyline`.
   - Modify the database configuration in `index.js` if necessary.
4. **Create Tables**: Run the SQL queries to create tables by executing the contents of `queries.sql`:
   ```bash
   psql -U your_username -d FamilyTravel -f queries.sql
  Replace your_username with your PostgreSQL username.

  
5. **Import Data**: Import data from `countries.csv` into the countries table:
    ```bash
    psql -U your_username -d FamilyTravel -c "\COPY countries FROM 'path/to/countries.csv' DELIMITER ',' CSV HEADER;"
  Replace your_username with your PostgreSQL username and path/to/countries.csv with the actual path to your CSV file.

   
7. Run the Application: Start the server using nodemon:
      ```bash
      nodemon index.js

8. Open your web browser and navigate to `http://localhost:3000` to use the application.

## Database Schema

The application uses the following database schema:

- **users**: Stores information about family members, including their name and preferred color
- **countries**: Contains a list of countries and their corresponding country codes.
- **visited_countries**: Represents the many-to-many relationship between family members and countries visited.

## Usage

- Visit the homepage to see the list of visited countries for the current family member.
- Use the "Add Country" form to add new countries to the current family member's visited list.
- Use the "Switch User" form to switch between different family members.
- To add a new family member, navigate to /user and click "New User."

## Contributions
  Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request.
