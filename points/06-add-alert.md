# how to add alert

- use `TempData`
- stay only for one request
- refresh and gone

# use TempData

- set data to `TempData` in `Controller`
- get data in `category/index` page
  ```
    @if(TempData["success"] != null){
    <h2>@TempData["success"]</h2>
  }
  ```
