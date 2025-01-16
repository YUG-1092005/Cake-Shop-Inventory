# Cake Shop Inventory Management System

This is a basic inventory management system for a cake shop implemented in Python. The program stores cake inventory data in a JSON file and allows users to interact with the menu, add items to their cart, view the cart, and generate a bill.

## Features

1. **Inventory Management**: 
   - The inventory contains information about various cakes and pastries, including their flavour, weight, price, type, and available quantity.
   - The inventory data is saved to a `Cake_Inventory.json` file for persistence.

2. **Customer Interaction**: 
   - **View Menu**: Customers can view the available cakes and pastries, including their details like flavour, weight, price, and quantity.
   - **Add to Cart**: Customers can select a cake by entering its ID and specify the quantity. The system ensures that the stock is sufficient for the order.
   - **View Cart**: Customers can view the items in their cart, including their details and quantities.
   - **Bill Generation**: Customers can generate a bill which includes the total amount, GST (18%), and any applicable discounts (2% off for orders above Rs. 500).

3. **Data Persistence**: 
   - The inventory data is stored in a JSON file (`Cake_Inventory.json`), allowing the data to persist across sessions.

4. **Dynamic Cart Updates**: 
   - The inventory is updated in real-time when an order is confirmed, reducing the stock based on the quantity ordered.

## Cake Inventory Structure

The inventory consists of a dictionary of cake items, each with the following attributes:

- **Flavour**: The flavour of the cake (e.g., Black Chocolate, Vanilla).
- **Weight**: The weight of the cake (e.g., 200gm, 50gm).
- **Price**: The price of the item in INR.
- **Type**: The type of cake or pastry (e.g., Cake, Pastry).
- **Quantity**: The available quantity in stock.

Example of the cake shop inventory:

```json
{
    "1001": {"flavour": "Black Chocolate", "weight": "200gm", "price": 200, "type": "Cake", "quantity": 4},
    "1002": {"flavour": "Vanilla", "weight": "50gm", "price": 100, "type": "Pastry", "quantity": 10},
    "1003": {"flavour": "Strawberry", "weight": "200gm", "price": 250, "type": "Cake", "quantity": 3},
    "1004": {"flavour": "White Chocolate", "weight": "300gm", "price": 300, "type": "Cake", "quantity": 5}
}
