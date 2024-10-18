# HotelBookingSystem
JAVA|JDBC|Mysql
This project demonstrates how to connect a Java application to a MySQL database using Maven. You can easily manage dependencies via the pom.xml file, eliminating the need to manually add JAR files to your build path.

Prerequisites
JDK 8 or later installed
Maven installed
MySQL database
MySQL JDBC Driver (added via Maven)
Setting Up the Project
Clone the repository (or create a Maven project manually):

bash
Copy code
git clone https://your-repository-url.git
cd your-project-directory
Configure the pom.xml:

Open the pom.xml file and add the MySQL connector dependency in the <dependencies> section:

xml
Copy code
<dependencies>
    <!-- MySQL Connector Java -->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.33</version>
    </dependency>
</dependencies>
This ensures that Maven will automatically download the required MySQL JDBC driver.

Database Setup:

Ensure you have a running MySQL instance. Create a database and note the following details:

Database name
Username
Password
Host (typically localhost)
Port (default 3306)
Update these details in the connection code within the App.java file.

Running the Application:

To run the application, use Maven commands:

Compile the project:

bash
Copy code
mvn compile
Run the application:

bash
Copy code
mvn exec:java -Dexec.mainClass="your.package.App"
Note: Ensure that the App.java class contains the correct main method and database connection logic.
