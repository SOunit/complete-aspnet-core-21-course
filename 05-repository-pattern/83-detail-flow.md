# unit of work

- coordinate the work of multiple repository
- create a single database context class

  - shared by all of them

- controller - unit of work - entity framework and database

- unit of work
  - repository
  - repository
  - DbContext

# argument - duplicate with Entity framework?

- DbSet = Repository
  - Add(obj)
  - Remove(obj)
  - Find(id)
  - FirstOrDefault(expression)
  - Where(expression)
- DbContext = Unit of Work

  - DbSet
  - DbSet
  - DbSet
  - SaveChanges()

# conclusion

- DbSet and DbContext looks like repository pattern
- but do not bring benefits so should follow repository pattern
  - less code duplication
  - independent from middleware

# tradeoff

- using pattern makes project consume more time
- not good with tight schedule and frequent requirement changes
