# Library App

## Description
Library App is a console application for managing library operations such as searching for patrons, viewing patron details, and managing loans. The application uses a JSON-based data storage system and follows a clean architecture with separation of concerns between the core logic, data access, and user interface.

## Project Structure
- `AccelerateDevGitHubCopilot.sln`
- `README.md`
- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
    - `Library.ApplicationCore.csproj`
  - `Library.Console/`
    - `CommonActions.cs`
    - `ConsoleApp.cs`
    - `ConsoleState.cs`
    - `Json/`
    - `Program.cs`
    - `appSettings.json`
    - `Library.Console.csproj`
  - `Library.Infrastructure/`
    - `Data/`
    - `Library.Infrastructure.csproj`
- `tests/`
  - `UnitTests/`
    - `ApplicationCore/`
    - `UnitTests.csproj`

## Key Classes and Interfaces
- **Library.ApplicationCore**
  - `Entities/`
    - `Patron`: Represents a library patron.
    - `Loan`: Represents a loan of a book item to a patron.
  - `Enums/`
    - `ConsoleState`: Enum representing the different states of the console application.
  - `Interfaces/`
    - `IPatronRepository`: Interface for patron data access.
    - `ILoanRepository`: Interface for loan data access.
    - `ILoanService`: Interface for loan-related operations.
    - `IPatronService`: Interface for patron-related operations.
  - `Services/`
    - `LoanService`: Implements `ILoanService` for managing loans.
    - `PatronService`: Implements `IPatronService` for managing patrons.

- **Library.Console**
  - `ConsoleApp`: Main class for managing the console application's state and interactions.
  - `CommonActions`: Enum representing common actions in the console application.
  - `Program`: Entry point for the console application.

- **Library.Infrastructure**
  - `Data/`
    - `JsonData`: Manages loading and saving data from/to JSON files.
    - `JsonLoanRepository`: Implements `ILoanRepository` for JSON-based data access.
    - `JsonPatronRepository`: Implements `IPatronRepository` for JSON-based data access.

## Usage
1. **Build the Solution**:
   ```sh
   dotnet build AccelerateDevGitHubCopilot.sln

/ ## License
This project is licensed under the MIT License
