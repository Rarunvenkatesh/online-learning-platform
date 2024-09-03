Step 1: Set Up Your Development Environment

1. Install Eclipse or IntelliJ IDE:
   - Download and install either Eclipse IDE or IntelliJ IDEA from their official websites.
   - Once installed, open the IDE.
   - Navigate to the File menu and select Open Project to open your project file.

Step 2: Install MySQL Server and MySQL Connector

1. Download MySQL Server:
   - Visit the official MySQL website and download the MySQL Server suitable for your operating system.
   - Follow the installation instructions to set up MySQL Server on your machine.
2. Download MySQL Connector/J:
   - Download the MySQL Connector/J (platform-independent) from the [MySQL website](https://dev.mysql.com/downloads/connector/j/).
   - Extract the downloaded file to access the `.jar` file.

Step 3: Integrate MySQL Connector/J with Your Project

1. Add MySQL Connector/J to Your Project:
   - In your IDE (Eclipse or IntelliJ IDEA), right-click on the project name in the **Project Explorer or Project View.
   - Select Properties (in Eclipse) or Modules (in IntelliJ IDEA).
   - Navigate to Java Build Path(in Eclipse) or Dependencies(in IntelliJ IDEA) and add the MySQL Connector/J `.jar` file to your project.

Step 4: Install and Configure XAMPP

1. Download XAMPP:
   - Visit the official [XAMPP website](https://www.apachefriends.org/index.html) and download the XAMPP package for your operating system.
   - Install XAMPP and launch the XAMPP Control Panel.
2. Start MySQL Server:
   - In the XAMPP Control Panel, click the  Start button next to MySQL to initiate the MySQL server.

 Step 5: Set Up MySQL Workbench

1.Open MySQL Workbench:
   - If you don't have MySQL Workbench installed, you can download it from the [MySQL website](https://dev.mysql.com/downloads/workbench/).
   - Open MySQL Workbench.
2. Create a NewConnection:
   - Click on the + icon next to MySQL Connections to create a new connection.
   - In the Connection Namenfield, enter a preferred name.
   - Set the Hostname to `localhost`.
   - Click OK to save the connection.

Step 6: Import the SQL Script

1. Open the New Connection:
   - Click on the newly created connection to open it.
2. Run the SQL Script:
   - Go to the File menu and select Run SQL Script
   - Browse and select the `.sql` file provided in your repository.
   - Click Start to execute the script and import the database schema and data.
   - Or Create the database manually by the given commands
Database: `online learning platform`
CREATE TABLE `coursetable` (
  `course_id` int(255) NOT NULL,
  `title` varchar(255) NOT NULL,
  `description` varchar(255) NOT NULL,
  `instructor` varchar(255) NOT NULL,
  `duration` int(255) NOT NULL
)
CREATE TABLE `enrollmenttable` (
  `enrollment_id` int(11) NOT NULL,
  `user_id` int(11) NOT NULL,
  `course_id` int(11) NOT NULL,
  `enrollment_date` date NOT NULL,
  `completion_date` date NOT NULL,
  `status` int(1) NOT NULL
)
CREATE TABLE `module` (
  `module_id` int(255) NOT NULL,
  `course_id` int(255) NOT NULL,
  `title` varchar(100) NOT NULL,
  `content` varchar(1000) NOT NULL,
  `duration` int(10) NOT NULL
)
CREATE TABLE `usertable` (
  `user_id` int(255) NOT NULL,
  `username` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `dob` date NOT NULL,
  `registration_date` date NOT NULL
) 

 Step 7: Run Your Java Project

1. Execute Your Code:
   - In Eclipse or IntelliJ IDEA, click the Run button (or use the `Run` menu) to execute your project.
   - The application should now connect to the MySQL database and function as expected.


