# constructor

```
using Microsoft.EntityFrameworkCore;

namespace BulkyBookWeb.Models.Data
{
    public class ApplicationDbContext : DbContext

    {
        // what is this?
        public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options) : base(options)
        {

        }
    }
}

```

# how to handle complex resource in ASP.NET core MVC?

- url is like this in ASP.NET core
  ```
    domain/Controller/Action
  ```
