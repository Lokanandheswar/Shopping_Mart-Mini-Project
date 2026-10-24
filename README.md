# Shopping Mart

A simple command-line shopping mart application built with Python. It provides separate Admin and User menus for managing products, registering users, shopping carts, and checkout.

## Features

### Admin
- Add products with a product ID, name, and price.
- Update a product's name and price using its product ID.
- Remove products using their product ID.
- View all available products.
- View registered users.

### User
- Register with a user ID, name, and email.
- View available products.
- Add products to the shopping cart.
- Remove products from the cart.
- View cart items and the total amount.
- Confirm checkout and place an order.

### Main Menu
- Open the Admin menu.
- Open the User menu.
- Exit the application.

## Requirements

- Python 3
- No external Python packages are required.

## Project File

```text
shopping-mart/
└── shopping_mart.py
```

## How to Run

1. Make sure Python 3 is installed.
2. Open a terminal or command prompt in the folder containing `shopping_mart.py`.
3. Run:

   ```bash
   python shopping_mart.py
   ```

   On some Windows installations, use:

   ```bash
   py shopping_mart.py
   ```

## How to Use

When the program starts, it displays:

```text
Welcome to your shopping mart
1.Admin
2.User
3.Exit
```

### Admin workflow

1. Select `1` from the main menu.
2. Choose an action from the Admin menu:
   - `1` — Add Products
   - `2` — Update Product
   - `3` — Remove Product
   - `4` — View Products
   - `5` — View Users
   - `6` — Exit the Admin menu
3. Enter the requested product details or product ID.

### User workflow

1. Select `2` from the main menu.
2. Enter a user ID. If that ID is not already registered, enter the user's name and email to register.
3. Choose an action from the User menu:
   - `1` — View Products
   - `2` — Add to Cart
   - `3` — Remove from Cart
   - `4` — View Cart
   - `5` — Checkout
   - `6` — Exit the User menu
4. During checkout, review the items and total, then enter `yes` to place the order.

## How It Works

The program stores its data in four Python lists:

- `product_list` — product IDs, names, and prices.
- `user_list` — user IDs, names, and email addresses.
- `cart_list` — products currently in the cart.
- `order_list` — copies of carts for orders confirmed at checkout.

All data is kept in memory while the program runs.

## Current Limitations

- **No permanent storage:** products, users, carts, and orders are lost when the program exits.
- **No password-based authentication:** entering a user ID is the only registration check.
- **Shared cart:** the program uses one global cart for all users, rather than a separate cart for each user.
- **Input validation:** menu choices are converted with `int()`. Non-numeric menu input can cause the program to stop with a `ValueError`.
- **Price handling:** prices are initially collected as strings and converted to integers when calculating totals. Use whole-number prices; decimal prices are not supported by the current total calculation.
- **Order history:** orders are stored in memory, but the program does not provide a menu option to view previous orders.
- **No payment integration:** checkout confirms an order but does not process a payment.
- **Product quantities:** the cart stores product entries, but does not track an explicit quantity field or inventory stock.

## Possible Improvements

- Validate menu choices and product prices before processing them.
- Store data in a database or files so it persists between runs.
- Add password-based user authentication.
- Maintain a separate cart for each user.
- Support decimal prices and explicit product quantities.
- Add an order-history option.
- Add stock management and payment processing if required.

## License

No license is specified in the current project file. Add a license separately if you intend to publish or distribute the project.
