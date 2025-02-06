# Cart Functionality - React

A simple cart functionality implementation in React. This project allows users to add, remove, and update quantities of items in their cart.

## Features

- Add items to the cart
- Remove items from the cart
- Update item quantities in the cart
- View total price calculation
- Responsive and easy-to-use UI

## Tech Stack

- **Frontend**: React.js
- **State Management**: React `useState`
- **Styling**: CSS (or Tailwind CSS if you're using it)

---

## Installation Guide

### Clone the Repository

To get started, clone the repository to your local machine:

```
git clone https://github.com/krisprajapati03/CartFunctionality.git
cd CartFunctionality
```

### Install Dependencies

Make sure you have **Node.js** and **npm** installed. Run the following command to install dependencies:

```
npm install
```

### Run the Project

Once dependencies are installed, start the development server:

```
npm start
```

Your app will be available at `http://localhost:3000`.

---

## Project Structure

```
CartFunctionality/
│── public/                    # Static assets (e.g., index.html)
│── src/                       # Source code
│   ├── components/            # React components (Cart, Product, etc.)
│   ├── App.js                 # Main application file
│   ├── index.js               # Entry point for React app
│   ├── styles.css             # Styles for the app
│── package.json               # Project dependencies and scripts
│── README.md                  # Project documentation
```

---

## Usage

### Adding Items to the Cart

To add an item to the cart, use the following code:

```javascript
const addToCart = (product) => {
  setCart((prevCart) => [...prevCart, product]);
};
```

### Removing Items from the Cart

To remove an item from the cart, use this code:

```javascript
const removeFromCart = (productId) => {
  setCart((prevCart) => prevCart.filter((item) => item.id !== productId));
};
```

### Updating Item Quantity

To update the quantity of an item:

```javascript
const updateQuantity = (productId, newQuantity) => {
  setCart((prevCart) =>
    prevCart.map((item) =>
      item.id === productId ? { ...item, quantity: newQuantity } : item
    )
  );
};
```

---

## Acknowledgements

- Inspired by online tutorials for building a cart functionality in React.
- This project is a learning exercise for **React.js**.

---
