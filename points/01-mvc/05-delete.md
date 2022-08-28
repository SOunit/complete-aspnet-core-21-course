# Id is null

- if any field in model is accessed, data will be populated
- if disable, not population happens
- to get Id, add Id input with hidden prop
  ```
    <input asp-for="Id" hidden />
  ```
