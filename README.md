## How to set up
To set up the project, open the terminal and run the following commands: `npm init -y` and `npm install sqlite3`. Additionally, you'll need to create a `server.js` file and install the necessary dependencies by running `npm install express` and `npm install ejs`.

## How to run the application
To run the application, open the terminal and enter the command `node server.js`.

## How to create a database
To create a database, start by creating a file named database.js. Inside this file, you need to add the following code: `const sqlite3 = require('sqlite3').verbose();` and `const db = new sqlite3.Database('database.db');`. Once you have saved the file, open your terminal and execute the command `node database.js.` This will create the database file named database.db. Afterward, open SQLiteStudio or another SQLite management tool. In the program, go to the "Add Database" option, and locate the database.db file within your project directory. This will allow you to connect to the database and manage it using the software.

## Description of the database schema 
In the database schema, I created two tables. The first table, named product, contains six columns: product_id, image, name, price, description, and category_id. In this table, product_id is the primary key with an integer data type, and it uses the AUTOINCREMENT keyword to automatically increase its value. The category_id is a foreign key with an integer data type and is set as NOT NULL to ensure every product is associated with a category. The image column is a BLOB, while name and description are TEXT fields set as NOT NULL. The price column is of the REAL data type.

The second table, named category, has two columns: category_id and category_name. Here, category_id is the primary key with an integer data type, also using AUTOINCREMENT for automatic value increment. The category_name is a TEXT field set as NOT NULL.

This database schema was designed to ensure data integrity by enforcing relationships between products and categories and using constraints like primary and foreign keys.