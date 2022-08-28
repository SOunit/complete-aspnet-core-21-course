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
