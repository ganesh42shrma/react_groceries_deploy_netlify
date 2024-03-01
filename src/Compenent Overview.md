# React Grocery List README

## App.js

The `App.js` file serves as the main component for the React Grocery List application, orchestrating the overall structure and functionality through the combination of various components.

### Dependencies

- React Hooks: `useState`, `useEffect`

### State

- `items`: Array representing the grocery list, initialized from local storage or an empty array.
- `newItem`: Value of the new item to be added to the grocery list.
- `search`: Search query for filtering items.

### Functions

- `addItem(item)`: Adds a new item to the list with a unique ID.
- `handleCheck(id)`: Toggles the checked state of an item.
- `handleDelete(id)`: Deletes a specific item.
- `handleSubmit(e)`: Handles form submission for adding a new item.

### Effects

- `useEffect`: Persists grocery list data to local storage when `items` state changes.

### Components

1. `<Header />`: Displays the title.
2. `<AddItem />`: Allows adding new items.
3. `<SearchItem />`: Provides a search bar.
4. `<Content />`: Displays main content, including the list of items.
5. `<Footer />`: Shows additional information about the list.

## AddItem.js

The `AddItem.js` file contains the `AddItem` component, responsible for adding new items to the grocery list.

### Dependencies

- React Icons: `FaPlus` from `react-icons/fa`
- React Hooks: `useRef`

### Props

- `newItem`: Value of the new item.
- `setNewItem`: Updates `newItem` state.
- `handleSubmit`: Handles form submission.

### Structure

- `form`: Main form for adding new items.
  - `label`: Describes the input field.
  - `input`: Field for entering the new item's name.
  - `button`: Button to submit the form.

### Functionality

- Form submission on "Enter" key or button click.
- Input field auto-focus on button click.
- Updates `newItem` state as the user types.

## Content.js

The `Content.js` file contains the `Content` component, rendering the main content of the application, including the list of items.

### Props

- `items`: Array of grocery items.
- `handleCheck`: Handles checkbox state changes.
- `handleDelete`: Handles item deletion.

### Structure

- `main`: Main container for the content.
  - `ItemList`: Displays grocery items with checkboxes and delete buttons.
  - Message if the list is empty.

## Footer.js

The `Footer.js` file contains the `Footer` component, displaying additional information about the grocery list, particularly the total number of items.

### Props

- `length`: Total number of items.

### Structure

- `footer`: Container for footer information.
  - `p`: Displays total item count with proper grammar.

## Header.js

The `Header.js` file contains the `Header` component, displaying the title at the top of the application.

### Props

- `title`: Title to be displayed.

### Structure

- `header`: Container for the header section.
  - `h1`: Displays the application title.

### Default Props

- Default title set to "Default Title" if not provided.

## ItemList.js

The `ItemList.js` file contains the `ItemList` component, rendering the list of grocery items using the `LineItem` component.

### Props

- `items`: Array of grocery items.
- `handleCheck`: Handles checkbox state changes.
- `handleDelete`: Handles item deletion.

### Structure

- `ul`: Unordered list container for grocery items.
  - `LineItem`: Renders each grocery item.

## LineItem.js

The `LineItem.js` file contains the `LineItem` component, rendering individual grocery items with functionality to mark as checked or delete.

### Props

- `item`: Object representing a grocery item.
- `handleCheck`: Handles checkbox state changes.
- `handleDelete`: Handles item deletion.

### Dependencies

- React Icons: `FaTrashAlt` from `react-icons/fa`

### Structure

- `li`: List item container for each grocery item.
  - `input`: Checkbox for marking as checked or unchecked.
  - `label`: Displays the item name, crossed out if checked.
  - `FaTrashAlt`: Icon button for deleting the item.

### Functionality

- Checkbox for marking items as checked or unchecked.
- Double-click on the item name to toggle checked state.
- Icon button to delete the item.

## SearchItem.js

The `SearchItem.js` file contains the `SearchItem` component, providing a search bar for filtering items in the grocery list.

### Props

- `search`: Search query for filtering items.
- `setSearch`: Updates the `search` state.

### Structure

- `form`: Form container for the search bar.
  - `label`: Describes the input field.
  - `input`: Field for entering the search query.

### Functionality

- Users can input a search query to filter items.
- Search bar dynamically updates the `search` state as the user types.
