<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meesho-Style E-Commerce Store - README</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: #1f2937;
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem 1rem;
            background-color: #f8f9fa;
        }
        .container {
            background: #ffffff;
            padding: 2.5rem;
            border-radius: 12px;
            border: 1px solid #e5e7eb;
            box-shadow: 0 4px 14px rgba(0, 0, 0, 0.06);
        }
        h1, h2, h3 {
            color: #111827;
            border-bottom: 1px solid #e5e7eb;
            padding-bottom: 0.4rem;
            margin-top: 1.8rem;
        }
        h1 {
            margin-top: 0;
            font-size: 2rem;
            color: #9f2089; /* Meesho-inspired accent */
        }
        code {
            background: #f3f4f6;
            padding: 3px 6px;
            border-radius: 4px;
            font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
            font-size: 0.88em;
            color: #be185d;
        }
        pre {
            background: #1e293b;
            color: #f8fafc;
            padding: 1rem;
            border-radius: 8px;
            overflow-x: auto;
            line-height: 1.45;
        }
        pre code {
            background: none;
            color: inherit;
            padding: 0;
        }
        .badge {
            display: inline-block;
            padding: 4px 10px;
            font-size: 12px;
            font-weight: 600;
            color: #fff;
            border-radius: 20px;
            margin-right: 6px;
            margin-bottom: 6px;
        }
        .badge-pink { background-color: #9f2089; }
        .badge-blue { background-color: #0284c7; }
        .badge-green { background-color: #16a34a; }
        .badge-orange { background-color: #d97706; }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1rem 0;
        }
        th, td {
            border: 1px solid #e5e7eb;
            padding: 10px 12px;
            text-align: left;
        }
        th {
            background-color: #f9fafb;
            font-weight: 600;
        }
        ul, ol { padding-left: 22px; }
        li { margin-bottom: 6px; }
        a { color: #9f2089; text-decoration: none; }
        a:hover { text-decoration: underline; }
    </style>
</head>
<body>
    <div class="container">
        <h1>🛍️ Your Store Name — Social E-Commerce Web App</h1>
        <p>
            <span class="badge badge-pink">Meesho-Style UI</span>
            <span class="badge badge-blue">HTML / CSS / JS</span>
            <span class="badge badge-orange">UPI &amp; COD Payments</span>
            <span class="badge badge-green">Google Sheets Sync</span>
        </p>
        <p>A modern, mobile-first e-commerce and reselling web application inspired by Meesho. Customers can browse multi-category products, add items to their cart, choose online (UPI/QR) or Cash on Delivery (COD) payment methods, and automatically save every order directly into <strong>Google Sheets</strong>.</p>

        <p><strong>🔗 Live Store Link:</strong> <a href="https://yourstorename.com" target="_blank">https://yourstorename.com</a></p>

        <h2>✨ Key Features</h2>
        <ul>
            <li><strong>Meesho-Style Product Catalog:</strong> Clean product cards with discount badges, ratings, category filters, and search bar.</li>
            <li><strong>Smart Shopping Cart:</strong> Add/remove items, update quantities, and auto-calculate total price and delivery charges.</li>
            <li><strong>Multiple Payment Options:</strong> Supports <strong>UPI (GPay / PhonePe / Paytm QR &amp; ID)</strong>, Online Payment, and <strong>Cash on Delivery (COD)</strong> with Transaction ID capture.</li>
            <li><strong>Automatic Google Sheets Integration:</strong> Every placed order and payment detail is instantly saved to a Google Sheet via <strong>Google Apps Script</strong>—no paid backend required.</li>
            <li><strong>WhatsApp Order Confirmation:</strong> Option for customers to send order summaries directly on WhatsApp after checkout.</li>
            <li><strong>100% Mobile Responsive:</strong> Optimized for smooth shopping on Android, iOS, and desktop browsers.</li>
        </ul>

        <h2>📁 Project Structure</h2>
        <pre><code>meesho-style-store/
├── index.html              # Home page with product grid &amp; categories
├── product.html            # Single product details page (optional)
├── cart.html               # Cart &amp; checkout page with payment options
├── css/
│   └── style.css           # Responsive styling &amp; mobile navigation
├── js/
│   ├── products.js         # Product catalog data (name, price, image, category)
│   ├── cart.js             # Cart logic &amp; price calculation
│   └── checkout.js         # Google Sheets API &amp; payment form submission
├── apps-script/
│   └── Code.gs             # Google Apps Script to save orders into Google Sheets
└── images/                 # Product photos, banners &amp; UPI QR code</code></pre>

        <h2>📊 Google Sheets Order Database Format</h2>
        <p>When a customer completes checkout, the following columns are automatically recorded in your Google Sheet:</p>
        <table>
            <thead>
                <tr>
                    <th>Column</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><code>Timestamp</code></td>
                    <td>Date and time when the order was placed</td>
                </tr>
                <tr>
                    <td><code>Order ID</code></td>
                    <td>Unique auto-generated order number (e.g., <code>ORD-1024</code>)</td>
                </tr>
                <tr>
                    <td><code>Customer Name</code></td>
                    <td>Full name of the buyer</td>
                </tr>
                <tr>
                    <td><code>Phone / WhatsApp</code></td>
                    <td>10-digit contact number</td>
                </tr>
                <tr>
                    <td><code>Delivery Address</code></td>
                    <td>Full shipping address with Pincode</td>
                </tr>
                <tr>
                    <td><code>Products &amp; Qty</code></td>
                    <td>Ordered item names, sizes, and quantities</td>
                </tr>
                <tr>
                    <td><code>Total Amount (₹)</code></td>
                    <td>Final payable order amount</td>
                </tr>
                <tr>
                    <td><code>Payment Mode</code></td>
                    <td><code>UPI / Online</code> or <code>Cash on Delivery (COD)</code></td>
                </tr>
                <tr>
                    <td><code>Payment Status / UTR</code></td>
                    <td>UPI Transaction ID (UTR) or <code>Pending (COD)</code></td>
                </tr>
            </tbody>
        </table>

        <h2>⚙️ Setup &amp; Installation</h2>
        <ol>
            <li><strong>Clone or Download:</strong>
                <pre><code>git clone https://github.com/yourusername/meesho-style-store.git</code></pre>
            </li>
            <li><strong>Set Up Google Sheets Backend:</strong>
                <ul>
                    <li>Create a new <strong>Google Sheet</strong> and add the column headers listed above in Row 1.</li>
                    <li>Go to <strong>Extensions &rarr; Apps Script</strong>, paste the code from <code>apps-script/Code.gs</code>, and deploy it as a <strong>Web App</strong> (Access: <em>Anyone</em>).</li>
                    <li>Copy the generated <strong>Web App URL</strong> and paste it into <code>js/checkout.js</code>.</li>
                </ul>
            </li>
            <li><strong>Configure Payment QR:</strong> Replace <code>images/upi-qr.png</code> with your own UPI QR code and update your UPI ID in <code>cart.html</code>.</li>
            <li><strong>Run Locally:</strong> Open <code>index.html</code> in your browser or launch with VS Code Live Server.</li>
        </ol>

        <h2>🛠️ Technologies Used</h2>
        <ul>
            <li><strong>Frontend:</strong> HTML5, CSS3 (Flexbox &amp; Grid), Vanilla JavaScript (ES6+)</li>
            <li><strong>Database:</strong> Google Sheets</li>
            <li><strong>Backend Connector:</strong> Google Apps Script (REST Webhook via <code>fetch()</code>)</li>
            <li><strong>Hosting:</strong> GitHub Pages / Netlify / Vercel</li>
        </ul>

        <h2>📞 Store Support &amp; Contact</h2>
        <ul>
            <li><strong>Email:</strong> <a href="mailto:support@yourstorename.com">support@yourstorename.com</a></li>
            <li><strong>WhatsApp Support:</strong> +91-XXXXXXXXXX</li>
            <li><strong>Location:</strong> India</li>
        </ul>
    </div>
</body>
</html>
