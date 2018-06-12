# LACERA .NET Interview Test
### ***Visual Studio/C#/MVC***

The purpose of this test is to gauge the candidate’s knowledge of C# and general development. It then allows the candidate to **show off their skills** of the different project types offered by Visual Studio. A passing test will show the candidate’s ability to select the appropriate framework classes to complete the task, and their knowledge on SOLID, DRY, and similar principles.

## Part 1

Given the following “CSV” file:

``` text
Employee Name, Birthdate, Salary, DateHired
“John Smith”, 12/1/1974, 50000, 1/1/2005
“Karl Johnson”, 3/3/1980, 45000, 4/4/2009
“Mark Stowell”, 2/30/1977, 58000a, 3/31/2001
“Tony Spronan”, 9/30/1962, , 3/31/2000
“Jan Seveg”, 6/1/1988, 80000, 2/30/2003
“Mark Twain”, 7/2/1968, -55532, 1/15/2006
“Wendall Smith”, 8/9/1972,,,
```

> [Download the CSV file here](https://raw.githubusercontent.com/lacera1/dotnet-test/master/employees.csv)

1. Create a new Visual Studio solution
2. Add a new project to the solution to be shared by other projects
3. Write a DTO or entity class that represents the fields in the file (string, date, decimal, date)
4. Write a service class that perform the parsing and returns a list of entities read (e.g., `IEnumerable<T>`)
5. Unit tests should cover at least 80% of the code (unit tests required, but coverage is optional, but a plus if done). The tests can be in MSTest, or nUnit.

### Business Rules
1. The first line (header line) should be ignored
2. Flag the record as **Invalid**, if:
   * An amount is invalid
   * A date is invalid
   * The field is missing
3. Any quotes should be removed
4. Salaries should be greater than zero

## Part 2
1.Add a new Console project application to the solution that:
  * Takes a file name as a start-up argument
  * Parses the file using the parsing class
  * Loops through the resulting list and writes each record to the screen:
    * Name
    * Birthdate
    * Salary
    * Hired On
    * Status  *(display 'invalid' or 'valid' based on business rules)*

## Part 3
1. Add a new MVC project application to the solution that:
   * Provides a page where the user can upload a CSV file to be parsed
   * Parses the file using the parsing class from the shared project
   * Stores the parsed data in to a SQL Server database (LocalDB or SQLLite can be used)
   * Reads the SQL database and display the records in the controller (Home for example)
   * Loops through the resulting list and writes each record to the Index view (you can use a `<table>` or `<div>`):
      * Name
      * Birthdate
      * Salary
      * Hired On
      * Status  *(display 'invalid' or 'valid' based on business rules)*
2. The application should use Dependency Injection with NInject, SimpleInjector, or Castle
3. The application code should be programmed against interfaces wherever possible
4. No security required

## Part 4
1. Review generated classes and explain what principles you applied and why
2. Explain what improvements, if any, you will make to the design

## Part 5
1. Create a repository in GitHub (accounts are free if you don't have one)
2. `Push` the project/solution to the GitHub repository
2. Send an email to epaz@lacera.com with the link to the repository to be cloned

If you have any questions, do not hesitate to contact LACERA at epaz@lacera.com.

`<End of Test>`
