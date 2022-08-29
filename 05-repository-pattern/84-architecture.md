# repository pattern architecture

- IRepository
  - define generic methods
- Repository

  - actual implementations
    - Add(obj)
    - Remove(obj)
    - Find(id)
    - FirstOrDefault(expression)
    - GetAll(expression)

- ICategoryRepository
- CategoryRepository

  - GetCategoryListForDropDown()

- IOrderHeaderRepository
- OrderHeaderRepository

- IUnitOfWork
- UnitOfWork
  - Category
  - OrderHeader
  - Save()

# review

- IRepository
- Repository
- IUnitOfWOrk
- UnitOfWork
