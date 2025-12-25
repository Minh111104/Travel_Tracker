# Travel Tracker ✈️🌏

A full-stack web application to track the countries you have visited. Enter a country name, and the map will highlight ("glow up") the country. Built with Node.js, Express, PostgreSQL, and EJS.

## Features

- Add a country you have visited by name.
- Visited countries are highlighted on the world map.
- Prevents duplicate entries and invalid country names.
- Reset your visited countries list.

## Setup

1. **Clone the repository**

   ```sh
   git clone <repo-url>
   ```

2. **Install dependencies**

    ```sh
    npm install
    ```

3. **Configure PostgreSQL**

- Create a database named `world`.

- Create the following tables:

    ```sh
    CREATE TABLE countries (
    country_code VARCHAR(2) PRIMARY KEY,
    country_name VARCHAR(100) NOT NULL
    );

    CREATE TABLE visited_countries (
    country_code VARCHAR(2) PRIMARY KEY REFERENCES countries(country_code)
    );
    ```

- Populate the `countries` table with country codes and names.

4. **Set your database credentials**

- Edit `index.js` and update the `db` connection config if needed.

5. **Run the app**

    ```sh
    node index.js
    ```

- Visit `http://localhost:3000` in your browser.

## Usage

- Enter a country name and click **ADD**.
- The country will be highlighted on the map if valid.
- Click **RESET** to clear all visited countries.

## License

This project is created for educational purpose.

