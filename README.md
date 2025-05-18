# coffee-shop-challenge
📄 README.md
markdown
Copy code
# ☕ Coffee Shop Challenge

A Python-based object-oriented project simulating a coffee shop system, involving three core classes: `Customer`, `Coffee`, and `Order`. This system models relationships between customers and the coffees they order.

---

## 📁 Project Structure

coffee-shop-challenge/
├── Pipfile
├── debug.py
├── customer.py
├── coffee.py
├── order.py
└── tests/
├── customer_test.py
├── coffee_test.py
└── order_test.py

markdown
Copy code

---

## 🧠 Domain Overview

- **Customer** has many **Orders**
- **Coffee** has many **Orders**
- **Order** belongs to one **Customer** and one **Coffee**
- This models a **many-to-many** relationship between Customers and Coffees.

---

## ✅ Requirements

### Models & Properties

#### `Customer`
- `__init__(self, name)`
  - Name must be a string between 1–15 characters.
- `name` property
  - Getter returns name
  - Setter enforces type and length

#### `Coffee`
- `__init__(self, name)`
  - Name must be a string with at least 3 characters.
- `name` property
  - Getter returns name
  - Name is immutable after initialization

#### `Order`
- `__init__(self, customer, coffee, price)`
  - `customer`: must be a `Customer` instance
  - `coffee`: must be a `Coffee` instance
  - `price`: must be a float between 1.0–10.0
- `price` property is immutable

---

## 🔁 Relationships

- `Order.customer` → returns Customer instance
- `Order.coffee` → returns Coffee instance
- `Customer.orders()` → list of their orders
- `Customer.coffees()` → unique coffees they've ordered
- `Coffee.orders()` → list of its orders
- `Coffee.customers()` → unique customers who ordered it

---

## 📊 Aggregates & Methods

- `Customer.create_order(coffee, price)`
- `Coffee.num_orders()` → returns count of orders
- `Coffee.average_price()` → returns average price (or 0)

---

## ⭐ Bonus

- `Customer.most_aficionado(coffee)` (classmethod)
  - Returns the Customer who has spent the most on that coffee
  - Returns `None` if no orders exist

---

## 🧪 Running Tests

Run all unit tests with:

```bash
python3 -m unittest discover -s tests
🔧 Setup Instructions
bash
Copy code
git clone git@github.com:<your-username>/coffee-shop-challenge.git
cd coffee-shop-challenge
pipenv install
pipenv shell
👨‍💻 Author
Built with ❤️ by [TREVOUR]

yaml
Copy code

---

Would you like me to personalize the README with your GitHub username and name?
















