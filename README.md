# Restaurant Ordering System (Microsoft Access)

A relational database built in Microsoft Access to manage end-to-end restaurant operations — including menu items, orders, payments, table reservations, staff records, and customer feedback.

## Features

- **Menu Management** – Categories and menu items with pricing and availability status
- **Order Processing** – Track orders, order details, quantities, and subtotals per item
- **Payment Tracking** – Record payment method, amount paid, and payment date per order
- **Table & Reservation Management** – Manage table capacity/status and customer reservations by guest count
- **Staff Records** – Store staff details, roles, and salary information
- **Customer Feedback** – Capture ratings and comments linked to customers

## Database Structure

The system consists of the following tables, connected through primary and foreign key relationships:

| Table | Description |
|---|---|
| `Categories` | Menu item categories |
| `MenuItems` | Items with price, category, and availability |
| `Customers` | Customer details (name, phone, address) |
| `Orders` | Order records linked to customers |
| `OrderDetails` | Line items for each order (item, quantity, subtotal) |
| `Payments` | Payment records linked to orders |
| `Tables` | Restaurant tables with capacity and status |
| `Reservations` | Table bookings linked to customers |
| `Staff` | Staff details, roles, and salary |
| `Feedback` | Customer ratings and comments |

## Key Relationships

- `Orders.CustomerID` → `Customers.CustomerID`
- `OrderDetails.OrderID` → `Orders.OrderID`
- `OrderDetails.ItemID` → `MenuItems.ItemID`
- `MenuItems.CategoryID` → `Categories.CategoryID`
- `Payments.OrderID` → `Orders.OrderID`
- `Reservations.CustomerID` → `Customers.CustomerID`
- `Reservations.TableID` → `Tables.TableID`
- `Feedback.CustomerID` → `Customers.CustomerID`

## Concepts Used

- Relational Database Design
- Normalization
- Primary & Foreign Key Relationships
- Data Integrity Constraints

## How to Open

1. Install Microsoft Access (or use Access Runtime if just viewing).
2. Open `Restaurant_ordering_system.accdb`.
3. Explore tables, relationships, and (if included) forms/queries from the navigation pane.

## File Structure

```
├── Restaurant_ordering_system.accdb   # Main Access database file
```

## Future Improvements

- Add forms for order entry and reservation booking
- Add queries/reports for daily sales and revenue summaries
- Migrate to SQL Server / MySQL for multi-user access
- Add user authentication for staff logins

## Author

Built as a learning project to practice relational database design and DBMS concepts.