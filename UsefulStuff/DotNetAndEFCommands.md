1. **Create a new console application**:
    ```sh
    dotnet new console -n <project_name>
    ```

2. **Create a new class library**:
    ```sh
    dotnet new classlib -n <library_name>
    ```

3. **Build a project**:
    ```sh
    dotnet build
    ```

4. **Run a project**:
    ```sh
    dotnet run
    ```

5. **Restore project dependencies**:
    ```sh
    dotnet restore
    ```

6. **Add a package to a project**:
    ```sh
    dotnet add package <package_name>
    ```

7. **Add a project reference**:
    ```sh
    dotnet add reference <path_to_project>
    ```

8. **List installed .NET SDKs**:
    ```sh
    dotnet --list-sdks
    ```

9. **List installed .NET runtimes**:
    ```sh
    dotnet --list-runtimes
    ```

10. **Publish a project**:
    ```sh
    dotnet publish -c Release -o <output_directory>
    ```

11. **Run unit tests**:
    ```sh
    dotnet test
    ```

12. **Create a new solution**:
    ```sh
    dotnet new sln -n <solution_name>
    ```

13. **Add a project to a solution**:
    ```sh
    dotnet sln <solution_name>.sln add <project_path>
    ```

14. **Remove a project from a solution**:
    ```sh
    dotnet sln <solution_name>.sln remove <project_path>
    ```

15. **Update .NET CLI to the latest version**:
    ```sh
    dotnet tool update -g dotnet-ef
    ```

1. **Install the EF Core CLI tools**:
    ```sh
    dotnet tool install --global dotnet-ef
    ```

2. **Add EF Core to a project**:
    ```sh
    dotnet add package Microsoft.EntityFrameworkCore
    dotnet add package Microsoft.EntityFrameworkCore.Design
    ```

3. **Create a new migration**:
    ```sh
    dotnet ef migrations add <MigrationName>
    ```

4. **Update the database to the latest migration**:
    ```sh
    dotnet ef database update
    ```

5. **Remove the last migration**:
    ```sh
    dotnet ef migrations remove
    ```

6. **List all migrations**:
    ```sh
    dotnet ef migrations list
    ```

7. **Generate a SQL script from migrations**:
    ```sh
    dotnet ef migrations script
    ```

8. **Update the database to a specific migration**:
    ```sh
    dotnet ef database update <MigrationName>
    ```

9. **Drop the database**:
    ```sh
    dotnet ef database drop
    ```

10. **Scaffold a DbContext and entity classes from an existing database**:
    ```sh
    dotnet ef dbcontext scaffold "<ConnectionString>" Microsoft.EntityFrameworkCore.SqlServer -o <OutputDirectory>
    ```
