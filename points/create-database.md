- config file

  - `appsetting.json`

- create database with code first approach
  1. add Model class.
  2. add connection string to `appconfig.json`
  - check database name in SSMS(Microsoft SQL Server Management Studio)
  3. add builder to `Program.cs`
  4. run `add-migration AddCategoryToDatabase`
  - install package `.Net tools`
  5. run `update-database`
  - add connection string `TrustServerCertificate=True;`
