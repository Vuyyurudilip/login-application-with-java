# login-application-with-java

Basic login form using Java Swing and JDBC to connect to a MySQL database.
The insert class serves as the entry point for the application. It establishes a connection to the MySQL database using the specified URL, username, and password.

The LoginApplication class extends JFrame and represents the login form UI. It contains UI components such as labels, text fields, and a login button.

The LoginApplication constructor sets up the UI components and registers an ActionListener on the login button. When the login button is clicked, the ActionListener is triggered and the validateLogin method is called.

The validateLogin method takes the entered username and password as parameters and performs a database query to validate the credentials. It prepares a SELECT query with placeholders for the username and password using a PreparedStatement. The placeholders are then set with the actual values using setString. The query is executed, and if the result set contains any rows, it indicates that the credentials are valid.

Depending on the validation result, a success message or an error message is displayed using JOptionPane.

The code uses try-with-resources to automatically close the PreparedStatement and handle any SQLException that may occur during the execution of the query.

 
