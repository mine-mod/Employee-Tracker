# Employee Tracker

## Description

The Employee Tracker application is designed to manage and track employee information. It allows users to view, add, and manage employee details, leveraging a PostgreSQL database for storage. The application is built using Node.js and PostgreSQL, and it provides a simple command-line interface for interaction.

## Features

- **View Employees**: Retrieve and display a list of all employees.
- **Add Employees**: Add new employees to the database with details such as name, role, and department.
- **Update Employees**: Modify existing employee details.
- **Delete Employees**: Remove employees from the database.

## Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/mine-mod/employee-tracker.git
   ```

2. **Navigate to the Project Directory**

   ```sh
   cd employee-tracker
   ```

3. **Install Dependencies**

   Make sure you have [Node.js](https://nodejs.org/) and [PostgreSQL](https://www.postgresql.org/) installed. Run the following command to install the required Node.js packages:

   ```sh
   npm install
   ```

4. **Set Up PostgreSQL**

   Create a PostgreSQL database for the application. You can do this using the `psql` command-line tool or any PostgreSQL client.

   ```sh
   createdb employee_tracker
   ```

   **Note:** Update the connection settings in your application to match your PostgreSQL setup.

5. **Configure Environment Variables**

   Create a `.env` file in the root directory of your project with the following content:

   **.env**
   ```env
   DB_USER=postgres
   DB_PASSWORD=your_password
   DB_HOST=localhost
   DB_PORT=5432
   DB_NAME=employee_tracker
   ```

   Replace `your_password` with the actual password for your PostgreSQL user.

## Usage

1. **Start the Application**

   Run the following command to start the application:

   ```sh
   node index.js
   ```

2. **Interact with the Application**

   The application will prompt you with a list of options. You can choose to view, add, update, or delete employee records.

   - **View Employees**: Displays a list of all employees.
   - **Add Employee**: Prompts you to enter employee details and adds them to the database.
   - **Update Employee**: Allows you to update details of an existing employee.
   - **Delete Employee**: Removes an employee from the database by their ID.

## Project Structure

- `index.js`: Main entry point of the application. Handles user input and interacts with the database.
- `db/`: Contains files related to database operations.
  - `connection.js`: Configures the PostgreSQL connection pool.
  - `queries.js`: Contains SQL queries for interacting with employee data.
- `.env`: Environment variables for database configuration.

## API Endpoints

The application provides an internal API for database operations:

- **GET /employees**  
  Retrieve all employees from the database.

- **POST /employees**  
  Add a new employee. The request body should include employee details.

- **PUT /employees/:id**  
  Update an existing employee by ID. The request body should include updated details.

- **DELETE /employees/:id**  
  Delete an employee by ID.

## Troubleshooting

- **Database Connection Error**: Ensure that PostgreSQL is running and that your credentials in the `.env` file are correct.
- **Missing Dependencies**: Run `npm install` to make sure all required packages are installed.
- **File Paths**: Verify that file paths in the code are correct and that all necessary files are present.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. Ensure your contributions adhere to the project's coding standards and include tests for new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


