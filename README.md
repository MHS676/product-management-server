# 🛠️ Product Management API

This is a RESTful API built using **Node.js**, **Express.js**, and **MongoDB** that allows managing products and categories with specific requirements such as auto-generating a unique product code.

---

## ✅ Features

- Create and manage products and categories
- Auto-generate product codes based on product name rules
- Update product availability, discount, and description
- Filter products by category and search by name
- Include final price after discount in responses
- Error handling and input validation
- Clean and maintainable structure

---

## 🧮 Product Code Generation Logic

The product code follows a specific format:

<hashed product name>-<start_index><substring><end_index>

Steps:

1. Find the **longest strictly increasing alphabetical substring** in the product name.
2. If multiple exist, concatenate them.
3. Get their **start and end index** from the original name.
4. Prefix it with a **SHA-256 hash (first 6 chars)** of the name.

📌 Example:  
For **"Alpha Sorter"**, result:  
`p48asd4-0alport8`



---

## 🔌 Installation & Setup


git clone https://github.com/MHS676/product-management-api
cd product-management-api
npm install

Create a .env file:
MONGO_URI=your_mongodb_connection_string
PORT=5000

Start the development server:
npm run dev


API Endpoints
Categories
Method	Endpoint	Description
POST	/categories	Create a new category
GET	/categories	Get all categories

Products
Method	Endpoint	    Description
POST	/products	    Create a new product
GET	    /products	    Get products (with filters)
PUT	    /products/:id	Update product status/details

Filtering & Searching
You can use query params:

/products?category=65e9c5...

/products?search=alpha

Database Design (MongoDB Schema)[
![Image](https://github.com/user-attachments/assets/bf2bedc0-58fe-43ea-a35c-52a39ec2f899)

This project was completed as part of a backend development challenge.

I’ve given my best effort to meet all requirements. Some areas might be improved with more time, but I’ve tried to follow clean code principles, handle errors properly, and meet all task goals.

📎 GitHub Link: https://github.com/MHS676/product-management-server

I humbly request you to consider my work and give me a chance.

Thank you 🙌

— Hasan Talukder
