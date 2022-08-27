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
