# to create database, create model

- create `Model` folder in project root
- create `Category` class in `Model` folder

  - add `DataAnnotation` for database configuration

    ```
    public class Category
    {
        [Key]
        public int Id { get; set; }

        [Required]
        public String Name { get; set; }

        public int DisplayOrder { get; set; }
    }
    ```

- add `connectionString` to access database
- add `ApplicationDbContext` class
  - add `Entity Framework Core` package
    - select project
    - open mouse menu
    - select `Manage MuGet Packages`
    - search for `entity framework core`
  - add `Entity Framework Core SQL server` package too
    - search `sql server`
  - add `Data` folder to project root
    - add `ApplicationDbContext` class
      - extend `DbContext`
        - to access database
      - add `Category` class
        - to create table
        ```
        public DbSet<Category> Category { get; set; }
        ```
- add database connection logic to `Program.cs`
  ```
  builder.Services.AddDbContext<ApplicationDbContext>(options => options.UseSqlServer(
        builder.Configuration.GetConnectionString("DefaultConnection")
    ));
  ```
- add constructor to `ApplicationDbContext` class
- crate migration file
  - install `tools` package
  - go to `tools/MuGetPackageManager/console`
  - `add-migration AddCategoryToDb`
- update database
  `update-database` in console
