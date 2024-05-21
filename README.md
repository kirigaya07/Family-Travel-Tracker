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
   - Create a PostgreSQL database named `FamilyTravel`.
   - Modify the database configuration in `app.js` if necessary.
4. **Create Tables**: Run the SQL queries to create tables by executing the contents of `queries.sql`:
   ```bash
   psql -U your_username -d FamilyTravel -f queries.sql
