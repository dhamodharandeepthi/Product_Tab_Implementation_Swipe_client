# Invoice Management System

## ProductsTab Component

### Overview

The **`ProductsTab`** component displays a list of items from all invoices. Users can view details of each item in a modal and delete items from the list. The component uses **`react-bootstrap`** for UI elements and **`react-redux`** for state management

### Features

- **Display Items:** Shows a list of items from all invoices in a table format.

- **View Details:** Opens a modal with detailed information about an item.

- **Delete Item:** Removes an item from the list.

### Dependencies

- **react-bootstrap:** For UI components and styling.

- **react-icons:** For icons (BiTrash, BsEyeFill).

- **react-redux:** For state management.

- **react-router-dom:** For navigation.

### Component Structure

#### `ProductsTab`

- **Purpose:** Renders a table of items from all invoices.

- **State:** None

- **Hooks:**

  - **`useInvoiceListData:`** Custom hook to fetch invoice list data from the Redux store.

  - **`useNavigate:`** For navigation.

- Child Component:

  - **`ItemRow:`** Renders each item with options to view details or delete.

#### `ItemRow`

- **Purpose:** Renders individual items with actions to view details or delete.

- **Props:**

  - **item:** Object containing item details.

  - **navigate:** Navigation function.

- **State:**

  - **isOpen:** Boolean to control the visibility of the modal.

- **Handlers:**

  - **handleDeleteClick:** Dispatches an action to delete the item.

  - **openModal:** Opens the modal to view item details.

  - **closeModal:** Closes the modal.

### InvoiceModal

- **Purpose:** Displays detailed information about an item.

- **Props:**

  - **showModal:** Boolean to control modal visibility.

  - **closeModal:** Function to close the modal.

  - **info:** Object containing invoice details.

  - **items:** Array of items to display in the modal.

  - **currency, subTotal, taxAmount, discountAmount, total:** Values to display.
