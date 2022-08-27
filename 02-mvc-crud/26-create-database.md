- create database
  - require SSMS / Microsoft SQL Server Management Studio
  - setup connection string in `appsetting.json`
  - use `Entity framework`
    - create `Data` folder under `Models` folder
    - `ApplicationDbContext.cs`
      - add constructor
      - add Dataset<Category> type categories with getter / setter
    - add builder code `Program.cs`
      ```
      builder.Services.AddDbContext<ApplicationDbContext>(options => options.UseSqlServer(builder.Configuration.GetConnectionString("DefaultConnection")));
      ```
      - install NuGet Package
        - `.Net EntityFramework SQL server`
    - add migration
      - open NuGet console
      - run command
        ```
        add-migration AddCategoryToDatabase
        ```
        - if error
          - Just install `Microsoft.EntityFrameworkCore.Tools` package from nuget:
            - ref
              https://stackoverflow.com/questions/38173404/the-term-add-migration-is-not-recognized
    - update database using migration file
      ```
      update-database
      ```
      - error
        - solve adding this to connection string
        ```
        TrustServerCertificate=True;
        ```
