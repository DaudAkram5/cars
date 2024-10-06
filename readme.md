# Cars Step 1

### 1. **Create a Car Class**

- Define a `Car` class with properties for the car's license plate, maker, model, current owner, price, and color.

### 2. **User Input for Car Details**

- Set up an HTML form for users to input the car's license plate, maker, model, current owner, price, and color.
- Use JavaScript to collect the values entered by the user when the form is submitted.

### 3. **Create and Store Car Objects**

- Upon form submission, instantiate a new `Car` object using the collected input values.
- Add this new `Car` object to an array that stores all the cars entered by the user.

### 4. **Display Car Information**

- Use JavaScript to dynamically generate a table on the webpage, displaying the information of each car in the array.
- Ensure the table updates to include each new car when it is added.

### 5. **Search for a Car by License Plate**

- Implement a function that allows the user to search for a car using its license plate.
- Include error handling to manage cases where the search input is invalid or the license plate cannot be found.

### 6. **Show Search Results**

- If the search successfully finds a car, display the car's make, model, and owner on the screen.
- If no matching car is found, display a message indicating that no results were found.

# Cars Step 2

### 7. **Refactor `Car` Class to Include Year**

- Add a new property `year` to the `Car` class to represent the year the car was manufactured.
- Modify the HTML form to include an additional field where the user can input the car's year.
- Update the form submission handler to collect the `year` value and pass it when creating a new `Car` object.

### 8. **Error Handling for Input Validation**

- Add error handling to ensure that all required fields (license plate, maker, model, current owner, price, color, and year) are provided by the user.
- Ensure that the `year` is a valid number and falls within a reasonable range (e.g., between 1886 and the current year).
- If invalid data is entered, display an error message on the screen and prevent the car from being added to the list.

  **Example checks:**

  - License plate must not be empty.
  - Price must be a positive number.
  - Year must be a number between 1886 and the current year.

### 9. **Discount Based on Car Year**

- Implement a feature that calculates a discount based on the car's age. Cars older than 10 years should receive a 15% discount on their price.
- Update the car display table to show both the original price and the discounted price (if applicable).
- Make sure to handle cases where the discount does not apply (i.e., cars that are less than 10 years old) and display the regular price.

### 10. **Refactor Search Function for Year-Based Discount**

- Update the search function to also display the discounted price (if applicable) when a car is found based on the license plate.
- If the car is older than 10 years, the search result should show both the original price and the discounted price.

### 11. **Additional Error Handling for Searching**

- Ensure that the search input is validated before attempting to find the car. For instance, the license plate should not be an empty string or contain invalid characters.
- If an invalid search input is provided, display an appropriate error message and do not proceed with the search.
- Handle cases where the car with the given license plate is not found and ensure the user is notified clearly.

# Cars Step 3

### 12. **Store Car Data**

- After adding a car to the list, ensure the car data is stored in LocalStorage to persist the list between page reloads.
  - Use `localStorage.setItem()` to store the cars array in LocalStorage as a JSON string.
- Ensure that whenever a car is added or deleted, LocalStorage is updated to reflect the current list of cars.
- After successfully adding a car, reset the form inputs and notify the user that the car has been added.
- When the page loads, retrieve any stored car data from LocalStorage.
  - Use `localStorage.getItem()` to retrieve the stored data and parse it back into an array using `JSON.parse()`.
- Repopulate the Car List: Once the car data is loaded from LocalStorage, repopulate the cars array in your application and update the display to show all the saved cars in the table.
- Handle Empty LocalStorage: If no cars are stored in LocalStorage, ensure the application starts with an empty car list without errors.

### 13. **Delete Car Functionality**

- Add a delete button for each car in the list. When clicked, the button should:
  - Remove the car from both the cars array and LocalStorage.
  - Dynamically update the table to remove the deleted car.
  - Update LocalStorage: After deleting a car, ensure the updated cars array is saved in LocalStorage using `localStorage.setItem()`.

### 14. **Enhanced Feedback**

- Provide clear feedback for the user when actions like adding or deleting a car occur.
  - Display a success message when a car is successfully added.
  - Show a confirmation message when a car is deleted.

### 15. **Form Improvements**

- Refine the form design to improve user experience and ensure it’s easy to use on both desktop and mobile devices.

### 16. **Table Display**

- Ensure the car table is responsive, clean, and displays the relevant car information clearly.

# Finalisation of the Project

### Acceptance Criteria

#### Functionality

- The user can add a car through a form and the data is stored in LocalStorage.
- The user can view the list of cars in a table, and the data persists across page reloads.
- The user can search for a car by license plate and view the details of the found car.
- The user can delete a car from the list, and the car is removed from both the UI and LocalStorage.

#### User Interface

- The application has a clean and modern design with consistent styling.
- Forms and buttons are visually appealing, with proper spacing, alignment, and validation feedback.
- The table is styled for readability, with alternating row colors and proper column spacing.
- The layout is responsive and adapts to different screen sizes, providing a good user experience on both desktop and mobile devices.

#### User Experience

- Error handling is in place for invalid inputs, with clear and user-friendly error messages.
- The interface is intuitive, with clear labels, buttons, and actions.
- Users receive feedback when performing actions (e.g., adding, searching, and deleting cars).
- The form resets after submission, improving user flow and preventing duplicate entries.
