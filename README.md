# inventory-management

Of course. Here are the instructions on how to run the application from a GitHub repository.

### Prerequisites

Before you begin, ensure you have the following installed on your system:

1.  **Node.js**: A JavaScript runtime environment. You can download it from [nodejs.org](https://nodejs.org/).
2.  **MySQL**: A relational database management system. You can download it from [mysql.com](https://www.mysql.com/).
3.  **Git**: A distributed version control system. You can download it from [git-scm.com](https://git-scm.com/).

### Step-by-Step Instructions

**1. Clone the Repository**

Open your terminal or command prompt and run the following command to clone the repository to your local machine. Replace `your-github-username/repository-name.git` with the actual URL of the repository.

```bash
git clone https://github.com/your-github-username/repository-name.git
cd repository-name
```

**2. Set Up the Database**

You need to create the database and the required tables.

*   **Log in to MySQL**:
    ```sql
    mysql -u your_username -p
    ```
*   **Create the database**:
    ```sql
    CREATE DATABASE inventorylocal;
    ```
*   **Use the database**:
    ```sql
    USE inventorylocal;
    ```
*   **Run the SQL scripts**: You will need to execute the SQL commands found in the `evolution/` directory to create the necessary tables.
    *   First, run the contents of `evolution/1.sql`.
    *   Then, run the contents of `evolution/2.sql`.

    You can do this by copying and pasting the content of each file into your MySQL client, or by using the `source` command:
    ```sql
    source /path/to/your/project/evolution/1.sql;
    source /path/to/your/project/evolution/2.sql;
    ```

**3. Configure the Application**

The application's configuration is located in the `config/` directory.

*   Open the `config/default.json` file.
*   Update the `database` section with your MySQL credentials (username, password, and database name).

```json
{
  "database": {
    "host": "localhost",
    "user": "your_mysql_username",
    "password": "your_mysql_password",
    "database": "inventorylocal"
  },
  "port": 15000
}
```

**4. Install Dependencies**

Navigate to the project's root directory in your terminal and run the following command to install all the required Node.js packages:

```bash
npm install
```

**5. Run the Application**

Once the dependencies are installed, you can start the server with this command:

```bash
npm start
```

You should see a message indicating that the server is listening on port `15000`.

**6. Access the Application**

Open your web browser and navigate to the following address:

[http://localhost:15000](http://localhost:15000)

You should now see the Inventory Management System login page. You can register a new user or use the "Demo Mode" to explore the application.

I will also create a new `RUN_INSTRUCTIONS.md` file with this information for you.
I have created the `RUN_INSTRUCTIONS.md` file with the setup and execution steps. Is there anything else you need?
