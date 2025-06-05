<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SELLING EVERYTHING</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: white;
      overflow-x: hidden;
    }
    header {
      text-align: center;
      padding: 40px 20px 10px;
    }
    header h1 {
      font-size: 42px;
      color: #00ffff;
      animation: glow 2s ease-in-out infinite alternate;
    }
    @keyframes glow {
      from { text-shadow: 0 0 5px #0ff; }
      to { text-shadow: 0 0 20px #0ff, 0 0 30px #0ff; }
    }
    header p {
      color: #ccc;
      margin-top: -10px;
    }
    .navbar {
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 15px 20px;
      background-color: #111;
      color: #aaa;
      font-size: 16px;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    .navbar div:hover {
      color: #00ffff;
      cursor: pointer;
      transform: scale(1.1);
      transition: 0.2s;
    }
    .products {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
      padding: 20px;
      animation: fadeInUp 0.8s ease-out;
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .product {
      background-color: #1a1a1a;
      border-radius: 15px;
      padding: 20px;
      width: 220px;
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.05);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      text-align: center;
    }
    .product:hover {
      transform: translateY(-10px);
      box-shadow: 0 0 20px rgba(0, 255, 255, 0.2);
      cursor: pointer;
    }
    .product img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    .form-container {
      background-color: #1a1a1a;
      margin-top: 20px;
      border-radius: 15px;
      padding: 20px;
      max-width: 400px;
      margin-left: auto;
      margin-right: auto;
      box-shadow: 0 0 15px rgba(255,255,255,0.1);
    }
    .hidden {
      display: none;
    }
    input, select, button {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: none;
      border-radius: 7px;
    }
    button {
      background-color: #00ffff;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.2s ease;
    }
    button:hover {
      background-color: #00cccc;
    }
    @media (max-width: 600px) {
      .products {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>
  <div class="navbar">
    <div onclick="location.reload()">Home</div>
    <div onclick="alert('Categories Coming Soon')">Categories</div>
    <div onclick="alert('Cart Coming Soon')">Cart</div>
  </div>
  <header>
    <h1>SELLING EVERYTHING</h1>
    <p>Featured Products</p>
  </header>  <div class="products">
    <div class="product" onclick="showDetails('Smart Speaker', 59)">
      <img src="https://via.placeholder.com/200x150?text=Speaker" alt="Smart Speaker">
      <h3>Smart Speaker</h3>
      <p>$59</p>
    </div>
    <div class="product" onclick="showDetails('Running Shoes', 129)">
      <img src="https://via.placeholder.com/200x150?text=Shoes" alt="Running Shoes">
      <h3>Running Shoes</h3>
      <p>$129</p>
    </div>
    <div class="product" onclick="showDetails('Smartwatch', 199)">
      <img src="https://via.placeholder.com/200x150?text=Smartwatch" alt="Smartwatch">
      <h3>Smartwatch</h3>
      <p>$199</p>
    </div>
  </div>  <div id="productDetails" class="form-container hidden">
    <h2 id="productName"></h2>
    <p id="productPrice"></p>
    <button onclick="showForm()">Buy Now</button>
  </div>  <div id="buyForm" class="form-container hidden">
    <h2>Enter Your Details</h2>
    <form id="orderForm">
      <input type="text" name="firstName" placeholder="First Name" required>
      <input type="text" name="lastName" placeholder="Last Name" required>
      <input type="text" name="address" placeholder="Address" required>
      <input type="text" name="phone" placeholder="Phone" required>
      <input type="text" name="city" placeholder="City" required><select id="paymentMethod" name="payment" required onchange="showPaymentInstructions()">
    <option value="">Select Payment Method</option>
    <option value="easypaisa">EasyPaisa</option>
    <option value="jazzcash">JazzCash</option>
    <option value="sadapay">SadaPay</option>
    <option value="cod">Cash on Delivery</option>
  </select>

  <div id="paymentInstructions" style="margin-top: 10px; color: #0ff;"></div>

  <button type="submit">I’ve Paid / Place Order</button>
</form>

  </div>  <script>
    let selectedProduct = {};

    function showDetails(name, price) {
      selectedProduct = { name, price };
      document.getElementById("productName").innerText = name;
      document.getElementById("productPrice").innerText = "$" + price;
      document.getElementById("productDetails").classList.remove("hidden");
      document.getElementById("buyForm").classList.add("hidden");
      window.scrollTo({ top: document.getElementById("productDetails").offsetTop, behavior: 'smooth' });
    }

    function showForm() {
      document.getElementById("buyForm").classList.remove("hidden");
      window.scrollTo({ top: document.getElementById("buyForm").offsetTop, behavior: 'smooth' });
    }

    function showPaymentInstructions() {
      const method = document.getElementById("paymentMethod").value;
      const instructionBox = document.getElementById("paymentInstructions");

      switch (method) {
        case 'easypaisa':
          instructionBox.innerHTML = `Pay to EasyPaisa number securely via your app.<br><strong>Business Account: Verified Merchant</strong>`;
          break;
        case 'jazzcash':
          instructionBox.innerHTML = `Send payment via JazzCash app.<br><strong>Business Account: Verified Merchant</strong>`;
          break;
        case 'sadapay':
          instructionBox.innerHTML = `Send payment using SadaPay.<br><strong>Account: Verified</strong>`;
          break;
        case 'cod':
          instructionBox.innerHTML = `You chose <strong>Cash on Delivery</strong>. Please keep the exact amount ready.`;
          break;
        default:
          instructionBox.innerHTML = '';
      }
    }

    document.getElementById("orderForm").addEventListener("submit", function (e) {
      e.preventDefault();
      const formData = new FormData(this);
      const data = {
        product: selectedProduct.name,
        price: selectedProduct.price,
        firstName: formData.get("firstName"),
        lastName: formData.get("lastName"),
        address: formData.get("address"),
        phone: formData.get("phone"),
        city: formData.get("city"),
        payment: formData.get("payment")
      };

      alert(`Thank you, ${data.firstName}! Your order for ${data.product} has been placed via ${data.payment.toUpperCase()}.`);
      document.getElementById("orderForm").reset();
      document.getElementById("buyForm").classList.add("hidden");
      document.getElementById("productDetails").classList.add("hidden");
    });
  </script></body>
</html>
