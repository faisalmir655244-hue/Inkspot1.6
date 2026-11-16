# 🛍️ Inkspot — Printing Press & Social E-Commerce Web App

![UI](https://img.shields.io/badge/UI-Meesho--Style-9f2089?style=for-the-badge)
![Tech](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JS-0284c7?style=for-the-badge)
![Payments](https://img.shields.io/badge/Payments-UPI%20%26%20COD-d97706?style=for-the-badge)
![Database](https://img.shields.io/badge/Sync-Google%20Sheets-16a34a?style=for-the-badge)

A modern, mobile-first e-commerce and custom printing web application inspired by Meesho. Customers can browse products, add items to their cart, pay via **UPI/QR** or **Cash on Delivery (COD)**, and every order is automatically recorded in **Google Sheets**.

🔗 **Live Store:** [https://yourstorename.com](https://yourstorename.com)

---

## ✨ Key Features

- **Meesho-Style Product Catalog:** Clean product cards with pricing, discount tags, category filters, and search.
- **Smart Shopping Cart:** Add/remove items, adjust quantities, and auto-calculate order totals.
- **Flexible Payment Options:** Supports **UPI (GPay / PhonePe / Paytm QR & ID)** with UTR/Transaction ID entry, as well as **Cash on Delivery (COD)**.
- **Automatic Google Sheets Sync:** Every order and payment detail is saved directly into a Google Sheet using **Google Apps Script**—no paid backend required.
- **WhatsApp Order Support:** Instant order confirmation and direct customer communication via WhatsApp.
- **100% Mobile Responsive:** Designed for smooth browsing on smartphones, tablets, and desktops.

---

## 📁 Project Structure

```text
Inkspot1.6/
├── index.html              # Main store page with product grid & categories
├── cart.html               # Cart & checkout page with payment options
├── css/
│   └── style.css           # Responsive styling & mobile layout
├── js/
│   ├── products.js         # Product catalog data (name, price, image, category)
│   ├── cart.js             # Cart management & price calculations
│   └── checkout.js         # Google Sheets API & payment form handler
├── apps-script/
│   └── Code.gs             # Google Apps Script to log orders in Google Sheets
└── images/                 # Product photos, banners & UPI QR code
