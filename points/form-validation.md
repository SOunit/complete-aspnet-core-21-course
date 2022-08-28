# server side validation

- error message to each input

  - model class has default validation
    - add span tag
    ```
    <span asp-validation-for="Name" class="text-danger"></span>
    ```

- error message as summary
  - add span tag
  ```
  <div asp-validation-summary="All"></div>
  ```

# client-side validation

- import validation logic
  ```
  @section Scripts{
  	@{
  		<partial name="_ValidationScriptsPartial" />
  	}
  }
  ```
