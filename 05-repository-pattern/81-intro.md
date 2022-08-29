# repository pattern

# benefit

- to avoid code duplication
- to get loose coupled code
  - easy to change from Entity Framework to another

# avoid duplicate sample

- traditional approach
  - same logic appear several times

```
    var CategorySelectList = _db.Category.Select(i => new SelectListItem(){
        Text = i.Name,
        Value = i.Id.toString()
    });
```

- repository pattern
  - logic stay 1 place only

```
    var CategorySelectList = _repository.GetCategoryListForDropDown();
```
