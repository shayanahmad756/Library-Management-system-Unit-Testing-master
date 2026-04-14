Library Management System Unit Testing
A simple Java-based library management system with unit testing using TestNG. The project demonstrates core object-oriented design for managing books, members, and borrowing flows, along with data-driven testing using Excel files through Apache POI.

Features
Add new books to the library
Add new members
List books and members
Check book availability
Borrow and return books
Run unit tests with TestNG
Use Excel-based test data for selected test cases
Tech Stack
Java 11
Maven
TestNG
Apache POI
Log4j2
Project Structure
src/
  main/
    java/library/
      Book.java
      Library.java
      LibraryManagementSystem.java
      LibraryManagementSystemMain.java
      Member.java
  test/
    java/test/
      BookTest.java
      BookTestExcel.java
      LibraryManagementSystemTest.java
      LibraryTest.java
      LibraryTestExcel.java
      MemberTest.java
    resources/
      BookExcel.xlsx
      LibraryData.xlsx
pom.xml
testng.xml
Main Components
Book: stores book ID, title, author, and availability status
Member: stores member information and supports borrow/return actions
Library: manages collections of books and members
LibraryManagementSystem: provides higher-level operations such as adding books, adding members, borrowing, returning, and availability checks
LibraryManagementSystemMain: console-based entry point for running the application
Prerequisites
Java JDK 11 or later
Maven 3.x
An IDE such as IntelliJ IDEA or Eclipse is optional
How to Run the Project
Clone the repository:
git clone https://github.com/your-username/library-management-system-unit-testing.git
cd library-management-system-unit-testing
Compile the project:
mvn clean compile
Run the console application:
mvn exec:java -Dexec.mainClass="library.LibraryManagementSystemMain"

If the Maven Exec plugin is not configured in your environment, you can run the main class directly from your IDE.

How to Run Tests
Run all Maven tests:

mvn test

Run the TestNG suite file:

mvn test -DsuiteXmlFile=testng.xml

Test Coverage
The test suite includes:

BookTest: getter/setter validation using TestNG data providers
LibraryTest: add/list/availability tests for books and members
MemberTest: borrow/return and member info tests
LibraryManagementSystemTest: service-level tests for adding books, adding members, and checking availability
BookTestExcel: Excel-driven test data for book scenarios
LibraryTestExcel: Excel-driven test data for combined library scenarios
Important Note
The Excel-based test classes currently use absolute file paths in:

src/test/java/test/BookTestExcel.java
src/test/java/test/LibraryTestExcel.java
If you upload this project to GitHub and run it on another machine, those paths will need to be changed to relative paths so the Excel tests work correctly after cloning.

Sample Use Cases
Register books in the library catalog
Add library members
Borrow available books
Return borrowed books
Verify business logic through automated tests
Future Improvements
Replace absolute test resource paths with relative classpath-based loading
Add more validations for invalid inputs
Store data in a database instead of memory
Improve console UI and exception handling
Add CI workflow for automated GitHub test runs
Author
Created for practice with Java, Maven, TestNG, and unit testing concepts.
