Classes Overview

1.ECommerceGUI
This is the main class responsible for the graphical user interface (GUI) of the application. It handles user interactions, displays product categories, manages the shopping cart, and processes orders. This class serves as the backbone of the application.

- Key Responsibilities:
  - Organizing the GUI layout.
  - Displaying product categories and products dynamically.
  - Adding items to the shopping cart and calculating totals.
  - Providing search and sort functionality.
  - Handling shopping cart operations like adding and removing items.


2.Product
This class represents individual products in the e-commerce platform. Each product has attributes like name, price, and category.

- Key Responsibilites:
  - Acts as a data model for each product.
  - Stores product details (name, price, and category) for display and calculations.
  - Facilitates filtering and sorting by category and price.


3.CartItem
This class represents an item in the shopping cart. It includes the product name, price, and the quantity of that product in the cart.

- Key Responsibilities:
  - Tracks the quantity of each product in the cart.
  - Provides methods for incrementing and decrementing quantities.
  - Helps calculate subtotals for each item in the cart.


Functionality Breakdown
1.ECommerceGUI

Initialization

- initializeProducts()
  - Purpose: Creates a list of all available products in the application.
  - Role: Centralizes the product data. All product-related actions (search, display, filtering) use this list.
  - Example: Adds "Laptop" under the "Electronics" category with a price of $1200.

Display Functions

- displayProductCategories()
  - Purpose: Displays a list of categories (e.g., "Electronics," "Produce," "Clothing") as buttons.
  - Role: Organizes products into logical sections, making navigation user-friendly.
  - Interaction: Clicking a category button calls `displayProductsByCategory()`.

- displayProductsByCategory(String category)
  - Purpose: Filters and displays products from a specific category.
  - Role: Shows products dynamically by creating buttons for each item in the selected category.
  - Interaction: Clicking a product button calls `addToCart()`.

- searchProducts()
  - Purpose: Allows users to search for products by name (case-insensitive).
  - Role: Uses Java Streams to filter products matching the search term.
  - Interaction: Displays filtered results dynamically; each result has a button to add the product to the cart.

Shopping Cart Functions

- addToCart(String name, double price)
  - Purpose: Adds a product to the shopping cart or increments its quantity if it's already in the cart.
  - Role: Updates the shopping cart list and recalculates the total price.
  - Interaction: Updates the cart dynamically and calls `updateTotalPriceLabel()`.

- removeFromCart(String name)
  - Purpose: Removes one instance of a product from the cart.
  - Role: Decreases the quantity of the item or removes it entirely if the quantity reaches zero.
  - Interaction: Recalculates totals and updates the cart display.

- displayShoppingCart()
  - Purpose: Displays all items in the cart, their quantities, and the subtotal.
  - Role: Provides a clear view of the user's selections and allows removal of items.
  - Interaction: Uses Java Streams for sorting and increment/decrement logic for modifying quantities.


Price Calculation Functions

- calculateShipping()
  - Purpose: Computes the shipping fee based on the total price. ($5 if the total exceeds $50, otherwise $10.)
  - Role: Ensures proper cost breakdown.

-calculateFinalTotal()
  - Purpose: Calculates the final total by adding tax and shipping fees to the base total.
  - Role: Reflects the true cost of the order.

- updateTotalPriceLabel()
  - Purpose: Updates the total price label on the GUI whenever the cart is modified.
  - Role: Keeps the user informed about their running total.


GUI Components

- JFrame, JPanel, JButton, JLabel
  - Purpose: Core components of Java Swing for creating a graphical interface.
  - Interaction: Used for displaying products, categories, and cart items dynamically.

2.Product

Attributes
- String name: The name of the product.
- double price: The price of the product.
- String category: The category the product belongs to (e.g., "Electronics," "Produce").

Key Methods
- Getters (getName(), getPrice(), getCategory()):
  - Provide access to product details for filtering, sorting, and displaying.


3.CartItem

Attributes
- String name: The name of the product in the cart.
- double price: The price of the product.
- int quantity: The quantity of the product in the cart.

Key Methods
- incrementQuantity():
  - Increases the quantity of the item by 1.
- decrementQuantity():
  - Decreases the quantity of the item by 1.
  - If the quantity reaches 0, the item is removed from the cart.


How They Work Together

Workflow Example

1. Navigation
   - The user clicks the "Products" button.
   - displayProductCategories() shows available categories like "Electronics" and "Clothing."

2. Selecting a Product
   - The user clicks a category (e.g., "Clothing").
   - displayProductsByCategory() filters and displays products in the selected category.

3. Adding to Cart
   - The user selects an item (e.g., "Jeans").
   - addToCart() adds the item to the shoppingCart list and updates the total.

4. Shopping Cart
   - The user views the cart via the "Go to Shopping Cart" button.
   - displayShoppingCart() lists items, calculates totals, and provides options to remove items.

5. Price Calculation
   - Tax and shipping fees are computed using calculateFinalTotal().

This modular design ensures the application is:
- Scalable: Adding new categories or products only requires modifying initializeProducts().
- Maintainable: Functions are focused and clearly defined, making debugging and updates straightforward.
- User-Friendly: The GUI dynamically updates, reflecting user actions like adding or removing items.
