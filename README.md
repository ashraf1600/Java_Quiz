# Java_Quiz
Course Code: CSE-202
Time: 30 minutes
Marks: 22.5

Suppose you have to create a movie review application where the user can see the ratings and reviews of the latest movies. A user can see the movie details, read the reviews, and give reviews. To give reviews, a user must sign up in the app and needs to log in. The signup requires the following information:
Name, Email, and Password

After login, clicking on a movie will show the list of reviews posted by other users. Users can provide a review so the review list will be sorted based on the highest upvote, lowest upvote, newly added, etc. There should be an option to add new reviews by the user. A user can review a movie only one time.

Your task is to sketch the layout or UI of this application. What tool will you use to design the frontend of this app and why? Will you need any database for this app? If your answer is yes, then mention the code for database connection.
Frontend Design Tool:
I will use Java Swing for designing the frontend because:

It is lightweight and platform-independent.
Swing provides a rich set of pre-built UI components such as buttons, text fields, tables, etc.
It easily integrates with Java backend logic, making it suitable for small to medium-scale applications.
Swing allows for event-driven programming, which simplifies user interaction handling.
# Ans
# Frontend Design Tool:
I will use Java Swing for designing the frontend because:

It is lightweight and platform-independent.
Swing provides a rich set of pre-built UI components such as buttons, text fields, tables, etc.
It easily integrates with Java backend logic, making it suitable for small to medium-scale applications.
Swing allows for event-driven programming, which simplifies user interaction handling.

 # Database Requirement:
Yes, a database is necessary for this app. It will store:

User Details: Name, Email, and Password for login and signup.
Movies: Movie names, ratings, and details.
Reviews: Reviews submitted by users, with upvotes, timestamps, and sorting preferences.
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;
# Database Connection Code:
// public class DatabaseConnection {
    public static Connection getConnection() {
        Connection connection = null;
        try {
      
            String url = "jdbc:mysql://localhost:3306/movie_review_app";
            String user = "root";
            String password = "your_password";

            // Establishing the connection
            connection = DriverManager.getConnection(url, user, password);
            System.out.println("Database connected successfully!");
        } catch (SQLException e) {
            System.err.println("Database connection failed!");
            e.printStackTrace();
        }
        return connection;
    }
}
# UI Layout of the Application:
# Signup Page:

Fields: Name, Email, Password.
Button: Signup.
Login Page:

Fields: Email, Password.
Buttons: Login, Signup.
Home Page:

Displays movie list with details, ratings, and reviews.
Allows users to click on a movie to view detailed reviews.
Movie Details Page:

Shows a list of reviews sorted by options (e.g., highest upvote, newest).
Includes a form to submit a new review (if the user hasn’t already).


