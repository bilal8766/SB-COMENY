<MOHD BILAL>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Salt Products</title>
    <meta name="description" content="SB COMENY - Premium quality salt products. Contact Mohd Bilal at 9813490892 or riyan.khan4712@gmail.com for more details.">
    <meta name="keywords" content="SB COMENY, salt, namak, Haryana, Mohd Bilal, business">
.auth-container {
    position: fixed;
    top: 15px;
    right: 20px;
    z-index: 999;
}

.auth-btn {
    background-color: #f44336; /* Red color matching theme */
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 0.9em;
    border-radius: 5px;
    cursor: pointer;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    transition: background-color 0.3s;
}

.auth-btn:hover {
    background-color: #d32f2f;
}

/* Auth Modal Specific Styles */
.auth-modal-content {
    max-width: 400px; /* Smaller width for login box */
    text-align: center;
}

.auth-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    border-bottom: 1px solid #eee;
    padding-bottom: 10px;
}

.auth-header h2 {
    margin: 0;
    color: #333;
}

.close-btn {
    font-size: 28px;
    font-weight: bold;
    color: #aaa;
    cursor: pointer;
}

.close-btn:hover {
    color: #333;
}

.auth-tabs {
    display: flex;
    margin-bottom: 20px;
    border-bottom: 2px solid #ddd;
}

.auth-tab {
    flex: 1;
    padding: 10px;
    background: none;
    border: none;
    cursor: pointer;
    font-size: 1em;
    color: #666;
    transition: all 0.3s;
}

.auth-tab.active {
    color: #f44336; /* Red active color */
    border-bottom: 3px solid #f44336;
    font-weight: bold;
}

.form-group {
    margin-bottom: 15px;
    text-align: left;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    color: #333;
    font-weight: bold;
    font-size: 0.9em;
}

.form-group input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
    font-size: 1em;
    box-sizing: border-box;
}

.submit-btn {
    background-color: #f44336;
    color: white;
    border: none;
    padding: 12px;
    font-size: 1em;
    border-radius: 5px;
    cursor: pointer;
    width: 100%;
    margin-top: 10px;
    transition: background-color 0.3s;
}

.submit-btn:hover {
    background-color: #d32f2f;
}
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin: 0;
            padding: 20px;
        }
        
        .logo {
            width: 150px;
            height: 150px;
            float: left;
        }
        
        @media (max-width: 600px) {
            .logo {
                width: 100px;
                height: 100px;
                float: none;
                margin: 0 auto 15px;
                display: block;
            }
        }
        
        .welcome-line {
            font-size: 1.5em;
            color: white;
            background-color: red;
            padding: 15px;
            margin: 20px 0;
            border-radius: 5px;
            clear: both;
        }
        
        h1 {
            color: #333;
            font-size: 2em;
            margin: 10px 0;
        }
        
        .personal-details {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px 0;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .photo {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 20px;
        }
        
        .details {
            text-align: left;
        }
        
        .details h2 {
            margin: 0 0 10px 0;
            color: #333;
            font-size: 1.2em;
        }
        
        .details p {
            margin: 5px 0;
            color: #666;
            font-size: 0.9em;
        }
        
        @media (max-width: 600px) {
            .personal-details {
                flex-direction: column;
                text-align: center;
            }
            
            .photo {
                margin-right: 0;
                margin-bottom: 15px;
            }
            
            .details {
                text-align: center;
            }
        }
        
        .product-section {
            margin: 30px 0;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            max-width: 1000px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .section-title {
            font-size: 1.5em;
            color: #333;
            margin: 20px 0;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .product-card {
            background-color: #f9f9f9;
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .product-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 5px;
            border: 2px solid #ddd;
        }
        
        .product-title {
            font-size: 1.1em;
            color: #333;
            margin-top: 15px;
        }
        
        .product-description {
            color: #666;
            margin-top: 10px;
            font-size: 0.85em;
        }
        
        .product-price {
            font-size: 1.3em;
            color: #4CAF50;
            font-weight: bold;
            margin-top: 10px;
        }
        
        .order-btn {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 0.9em;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 15px;
            transition: background-color 0.3s;
        }
        
        .order-btn:hover {
            background-color: #45a049;
        }
        
        /* Admin Button */
        .admin-btn {
            background-color: #333;
            color: white;
            border: none;
            padding: 8px 15px;
            font-size: 0.8em;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        
        /* Admin Panel Styles */
        .admin-panel {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            z-index: 2000;
        }
        
        .admin-content {
            background-color: white;
            margin: 2% auto;
            padding: 20px;
            border-radius: 10px;
            width: 95%;
            max-width: 1200px;
            height: 90vh;
            overflow-y: auto;
        }
        
        .admin-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #eee;
        }
        
        .admin-header h2 {
            color: #333;
        }
        
        .close-admin {
            font-size: 28px;
            font-weight: bold;
            color: #aaa;
            cursor: pointer;
        }
        
        .close-admin:hover {
            color: #333;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
        }
        
        .stat-card.green {
            background: linear-gradient(135deg, #4CAF50 0%, #2E7D32 100%);
        }
        
        .stat-card.red {
            background: linear-gradient(135deg, #f44336 0%, #c62828 100%);
        }
        
        .stat-card.orange {
            background: linear-gradient(135deg, #ff9800 0%, #ef6c00 100%);
        }
        
        .stat-card.purple {
            background: linear-gradient(135deg, #9c27b0 0%, #6a1b9a 100%);
        }
        
        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
        }
        
        .stat-label {
            font-size: 0.9em;
            margin-top: 5px;
        }
        
        .filter-section {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-bottom: 20px;
            padding: 15px;
            background-color: #f5f5f5;
            border-radius: 8px;
        }
        
        .filter-section input, .filter-section select {
            padding: 8px 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 0.9em;
        }
        
        .filter-section button {
            padding: 8px 15px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        
        .orders-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }
        
        .orders-table th, .orders-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        .orders-table th {
            background-color: #333;
            color: white;
            font-weight: bold;
        }
        
        .orders-table tr:hover {
            background-color: #f5f5f5;
        }
        
        .status-badge {
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.85em;
            font-weight: bold;
        }
        
        .status-pending {
            background-color: #fff3cd;
            color: #856404;
        }
        
        .status-completed {
            background-color: #d4edda;
            color: #155724;
        }
        
        .payment-badge {
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.85em;
            font-weight: bold;
        }
        
        .payment-cod {
            background-color: #e3f2fd;
            color: #1565c0;
        }
        
        .payment-phonepe {
            background-color: #f3e5f5;
            color: #7b1fa2;
        }
        
        .payment-googlepay {
            background-color: #e8f5e9;
            color: #2e7d32;
        }
        
        .action-btn {
            padding: 5px 10px;
            border: none;
            border-radius: 3px;
            cursor: pointer;
            font-size: 0.85em;
            margin-right: 5px;
        }
        
        .btn-complete {
            background-color: #4CAF50;
            color: white;
        }
        
        .btn-delete {
            background-color: #f44336;
            color: white;
        }
        
        .btn-view {
            background-color: #2196F3;
            color: white;
        }
        
        .clear-all-btn {
            background-color: #f44336;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-left: 10px;
        }
        
        /* Order Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }
        
        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 25px;
            border-radius: 10px;
            width: 95%;
            max-width: 500px;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .modal-header h2 {
            margin: 0;
            color: #333;
            font-size: 1.3em;
        }
        
        .close-btn {
            font-size: 28px;
            font-weight: bold;
            color: #aaa;
            cursor: pointer;
        }
        
        .close-btn:hover {
            color: #333;
        }
        
        .form-group {
            margin-bottom: 15px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #333;
            font-weight: bold;
            font-size: 0.9em;
        }
        
        .form-group input, .form-group textarea, .form-group select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1em;
            box-sizing: border-box;
        }
        
        .form-group textarea {
            resize: vertical;
            height: 70px;
        }
        
        /* Payment Options Styles */
        .payment-options {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        .payment-option {
            flex: 1;
            min-width: 120px;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            cursor: pointer;
            text-align: center;
            transition: all 0.3s;
            background-color: white;
        }
        
        .payment-option:hover {
            border-color: #4CAF50;
            background-color: #f5f5f5;
        }
        
        .payment-option.selected {
            border-color: #4CAF50;
            background-color: #e8f5e9;
        }
        
        .payment-option input {
            display: none;
        }
        
        .payment-icon {
            font-size: 1.5em;
            margin-bottom: 5px;
        }
        
        .payment-name {
            font-size: 0.9em;
            font-weight: bold;
            color: #333;
        }
        
        .payment-details {
            font-size: 0.75em;
            color: #666;
            margin-top: 3px;
        }
        
        .submit-btn {
            background-color: red;
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1em;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            transition: background-color 0.3s;
            margin-top: 10px;
        }
        
        .submit-btn:hover {
            background-color: #cc0000;
        }
        
        .loading {
            opacity: 0.7;
            pointer-events: none;
        }
        
        /* Order Summary */
        .order-summary {
            background-color: #f9f9f9;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 15px;
        }
        
        .order-summary h4 {
            margin: 0 0 10px 0;
            color: #333;
        }
        
        .order-summary p {
            margin: 5px 0;
            color: #666;
            font-size: 0.9em;
        }
        
        .order-summary .total {
            font-size: 1.2em;
            font-weight: bold;
            color: #4CAF50;
            margin-top: 10px;
            padding-top: 10px;
            border-top: 1px solid #ddd;
        }
        
        @media (max-width: 600px) {
            .orders-table {
                font-size: 0.75em;
            }
            
            .orders-table th, .orders-table td {
                padding: 6px;
            }
            
            .filter-section {
                flex-direction: column;
            }
            
            .filter-section input, .filter-section select {
                width: 100%;
            }
            
            .payment-option {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Custom SVG Logo for SB COMENY - Left Side -->
    <svg class="logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
        <circle cx="100" cy="100" r="90" fill="#4CAF50" stroke="#333" stroke-width="5"/>
        <text x="100" y="90" font-family="Arial, sans-serif" font-size="50" font-weight="bold" fill="red" text-anchor="middle">SB</text>
        <text x="100" y="120" font-family="Arial, sans-serif" font-size="18" fill="white" text-anchor="middle">COMENY</text>
    </svg>
    
    <div class="welcome-line">HELLO WELCOME MY COMPANY</div>
    
    <h1>SB COMENY</h1>
    <p>Premium quality salt products for your daily needs.</p>
    
    <!-- Admin Button -->
    <button class="admin-btn" onclick="openAdminPanel()">🔐 Admin Panel</button>
    
    <!-- Personal Details Section -->
    <div class="personal-details">
        <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg" alt="Mohd Bilal Profile Picture" class="photo">
        <div class="details">
            <h2>Mohd Bilal</h2>
            <p><strong>Mobile:</strong> +91 9813490892</p>
            <p><strong>Email:</strong> riyan.khan4712@gmail.com</p>
            <p><strong>Facebook:</strong> MOHD BILAL</p>
        </div>
    </div>
    
    <!-- Salt Products Section -->
    <h2 class="section-title">Our Salt Products</h2>
    
    <div class="product-section">
        <div class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/Generated%20Image.jpg" alt="SB COMENY Namak - 1 Kg Packet" class="product-image">
                <h3 class="product-title">SB COMENY Namak - 1 Kg</h3>
                <p class="product-description">Premium quality pure salt for your daily cooking needs.</p>
                <p class="product-price">₹25 / Packet</p>
                <button class="order-btn" onclick="openOrderModal('SB COMENY Namak - 1 Kg', '25')">Order Now</button>
            </div>
            
            <!-- Product 2 -->
            <div class="product-card">
                <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/WhatsApp%20Image%202026-01-06%20at%201.14.52%20PM.jpeg" alt="SB COMENY Premium Namak" class="product-image">
                <h3 class="product-title">SB COMENY Premium Salt</h3>
                <p class="product-description">High-quality refined salt for healthiest cooking.</p>
                <p class="product-price">₹35 / Packet</p>
                <button class="order-btn" onclick="openOrderModal('SB COMENY Premium Salt', '35')">Order Now</button>
            </div>
            
            <!-- Product 3 -->
            <div class="product-card">
                <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/3RD%20PRODUCT.jpeg" alt="SB COMENY Brand Banner" class="product-image">
                <h3 class="product-title">SB COMENY Brand</h3>
                <p class="product-description">Trusted salt brand from Haryana with pure quality.</p>
                <p class="product-price">₹50 / Packet</p>
                <button class="order-btn" onclick="openOrderModal('SB COMENY Brand', '50')">Order Now</button>
            </div>
        </div>
    </div>
    
    <!-- Admin Panel -->
    <div id="adminPanel" class="admin-panel">
        <div class="admin-content">
            <div class="admin-header">
                <h2>📊 Admin Dashboard - SB COMENY Orders</h2>
                <span class="close-admin" onclick="closeAdminPanel()">&times;</span>
            </div>
            
            <!-- Stats Cards -->
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number" id="totalOrders">0</div>
                    <div class="stat-label">Total Orders</div>
                </div>
                <div class="stat-card green">
                    <div class="stat-number" id="completedOrders">0</div>
                    <div class="stat-label">Completed</div>
                </div>
                <div class="stat-card orange">
                    <div class="stat-number" id="pendingOrders">0</div>
                    <div class="stat-label">Pending</div>
                </div>
                <div class="stat-card purple">
                    <div class="stat-number" id="codOrders">0</div>
                    <div class="stat-label">Cash on Delivery</div>
                </div>
                <div class="stat-card red">
                    <div class="stat-number" id="totalRevenue">₹0</div>
                    <div class="stat-label">Total Revenue</div>
                </div>
            </div>
            
            <!-- Filter Section -->
            <div class="filter-section">
                <input type="text" id="searchName" placeholder="Search customer name..." onkeyup="filterOrders()">
                <input type="text" id="searchProduct" placeholder="Search product..." onkeyup="filterOrders()">
                <input type="date" id="filterDate" onchange="filterOrders()">
                <select id="filterStatus" onchange="filterOrders()">
                    <option value="all">All Status</option>
                    <option value="pending">Pending</option>
                    <option value="completed">Completed</option>
                </select>
                <select id="filterPayment" onchange="filterOrders()">
                    <option value="all">All Payment</option>
                    <option value="COD">Cash on Delivery</option>
                    <option value="PhonePe">PhonePe</option>
                    <option value="GooglePay">Google Pay</option>
                </select>
                <button onclick="filterOrders()">🔍 Search</button>
                <button onclick="exportOrders()">📥 Export</button>
                <button class="clear-all-btn" onclick="clearAllOrders()">🗑️ Clear All</button>
            </div>
            
            <!-- Orders Table -->
            <table class="orders-table">
                <thead>
                    <tr>
                        <th>No</th>
                        <th>Date</th>
                        <th>Customer</th>
                        <th>Product</th>
                        <th>Qty</th>
                        <th>Price</th>
                        <th>Payment</th>
                        <th>Phone</th>
                        <th>Status</th>
                        <th>Action</th>
                    </tr>
                </thead>
                <tbody id="ordersTableBody">
                    <!-- Orders will be populated here -->
                </tbody>
            </table>
        </div>
    </div>
    
    <!-- Order Modal -->
    <div id="orderModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>Place Your Order</h2>
                <span class="close-btn" onclick="closeOrderModal()">&times;</span>
            </div>
            
            <!-- Order Summary -->
            <div class="order-summary">
                <h4>📦 Order Summary</h4>
                <p><strong>Product:</strong> <span id="summaryProduct">-</span></p>
                <p><strong>Price per packet:</strong> ₹<span id="summaryPrice">0</span></p>
                <p><strong>Quantity:</strong> <span id="summaryQuantity">1</span></p>
                <p class="total"><strong>Total: ₹<span id="summaryTotal">0</span></strong></p>
            </div>
            
            <form id="orderForm" onsubmit="submitOrder(event)">
                <input type="hidden" id="productName">
                <input type="hidden" id="productPrice">
                
                <div class="form-group">
                    <label for="customerName">Your Name:</label>
                    <input type="text" id="customerName" required placeholder="Enter your full name">
                </div>
                
                <div class="form-group">
                    <label for="customerPhone">Phone Number:</label>
                    <input type="tel" id="customerPhone" required placeholder="Enter your phone number">
                </div>
                
                <div class="form-group">
                    <label for="customerAddress">Delivery Address:</label>
                    <textarea id="customerAddress" required placeholder="Enter your full address"></textarea>
                </div>
                
                <div class="form-group">
                    <label for="quantity">Quantity (Packets):</label>
                    <input type="number" id="quantity" min="1" value="1" required onchange="updateOrderSummary()">
                </div>
                
                <!-- Payment Options -->
                <div class="form-group">
                    <label>Payment Mode:</label>
                    <div class="payment-options">
                        <div class="payment-option selected" onclick="selectPayment('COD', this)">
                            <input type="radio" name="paymentMode" value="COD" id="paymentCOD" checked>
                            <div class="payment-icon">💵</div>
                            <div class="payment-name">Cash on Delivery</div>
                            <div class="payment-details">Pay at delivery</div>
                        </div>
                        
                        <div class="payment-option" onclick="selectPayment('PhonePe', this)">
                            <input type="radio" name="paymentMode" value="PhonePe" id="paymentPhonePe">
                            <div class="payment-icon">📱</div>
                            <div class="payment-name">PhonePe</div>
                            <div class="payment-details">Pay via PhonePe</div>
                        </div>
                        
                        <div class="payment-option" onclick="selectPayment('GooglePay', this)">
                            <input type="radio" name="paymentMode" value="GooglePay" id="paymentGooglePay">
                            <div class="payment-icon">💳</div>
                            <div class="payment-name">Google Pay</div>
                            <div class="payment-details">Pay via GPay</div>
                        </div>
                    </div>
                </div>
                
                <!-- UPI Details Display (shown when online payment selected) -->
                <div id="upiDetails" style="display: none; background: #f0f0f0; padding: 10px; border-radius: 5px; margin-bottom: 15px; text-align: left;">
                    <p style="margin: 5px 0; font-size: 0.9em;"><strong>
                                        <p style="margin: 5px 0; font-size: 0.9em;"><strong>📱 UPI Payment Details:</strong></p>
                    <p style="margin: 5px 0; font-size: 0.85em;">UPI ID: <strong>riyan.khan4712@okhdfcbank</strong></p>
                    <p style="margin: 5px 0; font-size: 0.85em;">PhonePe/GooglePay: <strong>9813490892</strong></p>
                    <p style="margin: 5px 0; font-size: 0.85em; color: #666;">💡 After payment, please send screenshot on WhatsApp: <strong>+91 9813490892</strong></p>
                </div>
                
                <button type="submit" class="submit-btn">✅ Confirm Order</button>
            </form>
        </div>
    </div>
    
    <!-- Success Modal -->
    <div id="successModal" class="modal">
        <div class="modal-content" style="text-align: center; max-width: 400px;">
            <div style="font-size: 50px; margin-bottom: 15px;">✅</div>
            <h2 style="color: #4CAF50;">Order Placed Successfully!</h2>
            <p style="color: #666; margin: 15px 0;">Thank you for your order. We will contact you shortly.</p>
            <p style="font-size: 0.9em; color: #333;"><strong>Order ID:</strong> <span id="successOrderId">-</span></p>
            <button class="submit-btn" onclick="closeSuccessModal()" style="margin-top: 20px;">Close</button>
        </div>
    </div>
    
    <!-- Order Details Modal for Admin -->
    <div id="orderDetailsModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2>📋 Order Details</h2>
                <span class="close-btn" onclick="closeOrderDetailsModal()">&times;</span>
            </div>
            <div id="orderDetailsContent">
                <!-- Order details will be populated here -->
            </div>
        </div>
    </div>
    
    <script>
        // Initialize orders from localStorage or empty array
        let orders = JSON.parse(localStorage.getItem('sbComenyOrders')) || [];
        
        // Order counter for unique IDs
        let orderCounter = parseInt(localStorage.getItem('sbComenyOrderCounter')) || 1;
        
        // Admin password (simple client-side check)
        const ADMIN_PASSWORD = 'bilal@3691';
        
        // Function to open Admin Panel
        function openAdminPanel() {
            const password = prompt('Enter Admin Password:');
            if (password === ADMIN_PASSWORD) {
                document.getElementById('adminPanel').style.display = 'block';
                updateAdminStats();
                renderOrdersTable();
            } else if (password !== null) {
                alert('Incorrect Password!');
            }
        }
        
        // Function to close Admin Panel
        function closeAdminPanel() {
            document.getElementById('adminPanel').style.display = 'none';
        }
        
        // Function to open Order Modal
        function openOrderModal(productName, price) {
            document.getElementById('orderModal').style.display = 'block';
            document.getElementById('productName').value = productName;
            document.getElementById('productPrice').value = price;
            document.getElementById('summaryProduct').textContent = productName;
            document.getElementById('summaryPrice').textContent = price;
            document.getElementById('summaryQuantity').textContent = '1';
            document.getElementById('summaryTotal').textContent = price;
            document.getElementById('quantity').value = 1;
        }
        
        // Function to close Order Modal
        function closeOrderModal() {
            document.getElementById('orderModal').style.display = 'none';
            document.getElementById('orderForm').reset();
            document.getElementById('upiDetails').style.display = 'none';
            // Reset payment options
            document.querySelectorAll('.payment-option').forEach(opt => opt.classList.remove('selected'));
            document.querySelector('.payment-option').classList.add('selected');
        }
        
        // Function to close Success Modal
        function closeSuccessModal() {
            document.getElementById('successModal').style.display = 'none';
        }
        
        // Function to close Order Details Modal
        function closeOrderDetailsModal() {
            document.getElementById('orderDetailsModal').style.display = 'none';
        }
        
        // Function to select payment option
        function selectPayment(method, element) {
            // Remove selected class from all options
            document.querySelectorAll('.payment-option').forEach(opt => opt.classList.remove('selected'));
            // Add selected class to clicked option
            element.classList.add('selected');
            // Check the corresponding radio button
            document.querySelector(`input[value="${method}"]`).checked = true;
            
            // Show/hide UPI details
            const upiDetails = document.getElementById('upiDetails');
            if (method === 'PhonePe' || method === 'GooglePay') {
                upiDetails.style.display = 'block';
            } else {
                upiDetails.style.display = 'none';
            }
        }
        
        // Function to update order summary
        function updateOrderSummary() {
            const quantity = document.getElementById('quantity').value;
            const price = document.getElementById('productPrice').value;
            const total = quantity * price;
            
            document.getElementById('summaryQuantity').textContent = quantity;
            document.getElementById('summaryTotal').textContent = total;
        }
        
        // Function to submit order
        function submitOrder(event) {
            event.preventDefault();
            
            const orderId = 'ORD-' + orderCounter++;
            localStorage.setItem('sbComenyOrderCounter', orderCounter);
            
            const order = {
                id: orderId,
                date: new Date().toLocaleDateString('en-GB'),
                time: new Date().toLocaleTimeString('en-GB'),
                customerName: document.getElementById('customerName').value,
                customerPhone: document.getElementById('customerPhone').value,
                customerAddress: document.getElementById('customerAddress').value,
                product: document.getElementById('productName').value,
                price: document.getElementById('productPrice').value,
                quantity: document.getElementById('quantity').value,
                total: document.getElementById('summaryTotal').textContent,
                paymentMode: document.querySelector('input[name="paymentMode"]:checked').value,
                status: 'pending'
            };
            
            orders.push(order);
            localStorage.setItem('sbComenyOrders', JSON.stringify(orders));
            
            // Close order modal and show success
            closeOrderModal();
            document.getElementById('successOrderId').textContent = orderId;
            document.getElementById('successModal').style.display = 'block';
        }
        
        // Function to update admin stats
        function updateAdminStats() {
            const totalOrders = orders.length;
            const completedOrders = orders.filter(o => o.status === 'completed').length;
            const pendingOrders = orders.filter(o => o.status === 'pending').length;
            const codOrders = orders.filter(o => o.paymentMode === 'COD').length;
            const totalRevenue = orders
                .filter(o => o.status === 'completed')
                .reduce((sum, o) => sum + parseInt(o.total), 0);
            
            document.getElementById('totalOrders').textContent = totalOrders;
            document.getElementById('completedOrders').textContent = completedOrders;
            document.getElementById('pendingOrders').textContent = pendingOrders;
            document.getElementById('codOrders').textContent = codOrders;
            document.getElementById('totalRevenue').textContent = '₹' + totalRevenue;
        }
        
        // Function to render orders table
        function renderOrdersTable() {
            const tbody = document.getElementById('ordersTableBody');
            tbody.innerHTML = '';
            
            const filteredOrders = getFilteredOrders();
            
            filteredOrders.forEach((order, index) => {
                const tr = document.createElement('tr');
                
                tr.innerHTML = `
                    <td>${index + 1}</td>
                    <td>${order.date}<br><small style="color: #666;">${order.time}</small></td>
                    <td>${order.customerName}</td>
                    <td>${order.product}</td>
                    <td>${order.quantity}</td>
                    <td>₹${order.total}</td>
                    <td><span class="payment-badge payment-${order.paymentMode.toLowerCase()}">${order.paymentMode}</span></td>
                    <td>${order.customerPhone}</td>
                    <td><span class="status-badge status-${order.status}">${order.status.charAt(0).toUpperCase() + order.status.slice(1)}</span></td>
                    <td>
                        <button class="action-btn btn-view" onclick="viewOrderDetails('${order.id}')">View</button>
                        ${order.status === 'pending' ? `<button class="action-btn btn-complete" onclick="completeOrder('${order.id}')">✓</button>` : ''}
                        <button class="action-btn btn-delete" onclick="deleteOrder('${order.id}')">✗</button>
                    </td>
                `;
                
                tbody.appendChild(tr);
            });
            
            if (filteredOrders.length === 0) {
                tbody.innerHTML = '<tr><td colspan="10" style="text-align: center; padding: 30px; color: #666;">No orders found</td></tr>';
            }
        }
        
        // Function to get filtered orders
        function getFilteredOrders() {
            const searchName = document.getElementById('searchName').value.toLowerCase();
            const searchProduct = document.getElementById('searchProduct').value.toLowerCase();
            const filterDate = document.getElementById('filterDate').value;
            const filterStatus = document.getElementById('filterStatus').value;
            const filterPayment = document.getElementById('filterPayment').value;
            
            return orders.filter(order => {
                const matchName = order.customerName.toLowerCase().includes(searchName);
                const matchProduct = order.product.toLowerCase().includes(searchProduct);
                const matchDate = !filterDate || order.date === filterDate.split('/').reverse().join('/');
                const matchStatus = filterStatus === 'all' || order.status === filterStatus;
                const matchPayment = filterPayment === 'all' || order.paymentMode === filterPayment;
                
                return matchName && matchProduct && matchDate && matchStatus && matchPayment;
            });
        }
        
        // Function to filter orders
        function filterOrders() {
            updateAdminStats();
            renderOrdersTable();
        }
        
        // Function to view order details
        function viewOrderDetails(orderId) {
            const order = orders.find(o => o.id === orderId);
            if (!order) return;
            
            const content = document.getElementById('orderDetailsContent');
            content.innerHTML = `
                <div class="form-group">
                    <label><strong>Order ID:</strong></label>
                    <p>${order.id}</p>
                </div>
                <div class="form-group">
                    <label><strong>Date & Time:</strong></label>
                    <p>${order.date} at ${order.time}</p>
                </div>
                <div class="form-group">
                    <label><strong>Customer Name:</strong></label>
                    <p>${order.customerName}</p>
                </div>
                <div class="form-group">
                    <label><strong>Phone Number:</strong></label>
                    <p>${order.customerPhone}</p>
                </div>
                <div class="form-group">
                    <label><strong>Delivery Address:</strong></label>
                    <p>${order.customerAddress}</p>
                </div>
                <div class="form-group">
                    <label><strong>Product:</strong></label>
                    <p>${order.product}</p>
                </div>
                <div class="form-group">
                    <label><strong>Quantity:</strong></label>
                    <p>${order.quantity} packet(s)</p>
                </div>
                <div class="form-group">
                    <label><strong>Total Amount:</strong></label>
                    <p style="font-size: 1.2em; color: #4CAF50;">₹${order.total}</p>
                </div>
                <div class="form-group">
                    <label><strong>Payment Mode:</strong></label>
                    <p><span class="payment-badge payment-${order.paymentMode.toLowerCase()}">${order.paymentMode}</span></p>
                </div>
                <div class="form-group">
                    <label><strong>Order Status:</strong></label>
                    <p><span class="status-badge status-${order.status}">${order.status.charAt(0).toUpperCase() + order.status.slice(1)}</span></p>
                </div>
            `;
            
            document.getElementById('orderDetailsModal').style.display = 'block';
        }
        
        // Function to complete order
        function completeOrder(orderId) {
            const order = orders.find(o => o.id === orderId);
            if (order) {
                order.status = 'completed';
                localStorage.setItem('sbComenyOrders', JSON.stringify(orders));
                updateAdminStats();
                renderOrdersTable();
            }
        }
        
        // Function to delete order
        function deleteOrder(orderId) {
            if (confirm('Are you sure you want to delete this order?')) {
                orders = orders.filter(o => o.id !== orderId);
                localStorage.setItem('sbComenyOrders', JSON.stringify(orders));
                updateAdminStats();
                renderOrdersTable();
            }
        }
        
        // Function to clear all orders
        function clearAllOrders() {
            if (confirm('Are you sure you want to delete ALL orders? This action cannot be undone!')) {
                orders = [];
                localStorage.setItem('sbComenyOrders', JSON.stringify(orders));
                orderCounter = 1;
                localStorage.setItem('sbComenyOrderCounter', 1);
                updateAdminStats();
                renderOrdersTable();
            }
        }
        
        // Function to export orders to CSV
        function exportOrders() {
            const filteredOrders = getFilteredOrders();
            
            if (filteredOrders.length === 0) {
                alert('No orders to export!');
                return;
            }
            
            let csv = 'Order ID,Date,Time,Customer Name,Phone,Address,Product,Quantity,Total,Payment Mode,Status\n';
            
            filteredOrders.forEach(order => {
                csv += `"${order.id}","${order.date}","${order.time}","${order.customerName}","${order.customerPhone}","${order.customerAddress.replace(/"/g, '""')}","${order.product}","${order.quantity}","${order.total}","${order.paymentMode}","${order.status}"\n`;
            });
            
            const blob = new Blob([csv], { type: 'text/csv' });
            const url = window.URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'sb_comeny_orders_' + new Date().toISOString().slice(0, 10) + '.csv';
            a.click();
            window.URL.revokeObjectURL(url);
        }
        
        // Close modals when clicking outside
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
            }
        }
        
        // Auto-refresh admin stats every 30 seconds
        setInterval(() => {
            if (document.getElementById('adminPanel').style.display === 'block') {
                updateAdminStats();
                renderOrdersTable();
            }
        }, 30000);
    </script>
    <!-- Login / Register Button (Top Right) -->
<div class="auth-container">
    <button id="authBtn" class="auth-btn">Login / Register</button>
</div>

<!-- Login / Register Modal -->
<div id="authModal" class="modal">
    <div class="modal-content auth-modal-content">
        <div class="auth-header">
            <h2 id="authTitle">Login</h2>
            <span class="close-btn" onclick="closeAuthModal()">&times;</span>
        </div>
        
        <!-- Tab Buttons -->
        <div class="auth-tabs">
            <button class="auth-tab active" onclick="switchTab('login')">Login</button>
            <button class="auth-tab" onclick="switchTab('register')">Register</button>
        </div>

        <!-- Login Form -->
        <div id="loginForm">
            <form onsubmit="event.preventDefault(); alert('Login Successful!'); closeAuthModal();">
                <div class="form-group">
                    <label>Username</label>
                    <input type="text" placeholder="Enter username" required>
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" placeholder="Enter password" required>
                </div>
                <button type="submit" class="submit-btn">Login</button>
            </form>
        </div>

        <!-- Register Form -->
        <div id="registerForm" style="display: none;">
            <form onsubmit="event.preventDefault(); alert('Registration Successful!'); switchTab('login');">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" placeholder="Enter full name" required>
                </div>
                <div class="form-group">
                    <label>Email</label>
                    <input type="email" placeholder="Enter email" required>
                </div>
                <div class="form-group">
                    <label>Username</label>
                    <input type="text" placeholder="Choose username" required>
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" placeholder="Choose password" required>
                </div>
                <button type="submit" class="submit-btn">Register</button>
            </form>
        </div>
    </div>
</div>
// Get Modal Element
var modal = document.getElementById("authModal");
var authBtn = document.getElementById("authBtn");
var loginForm = document.getElementById("loginForm");
var registerForm = document.getElementById("registerForm");
var authTitle = document.getElementById("authTitle");
var tabs = document.querySelectorAll(".auth-tab");

// Open Modal on Button Click
authBtn.onclick = function() {
    modal.style.display = "block";
}

// Close Modal Function
function closeAuthModal() {
    modal.style.display = "none";
}

// Close Modal if clicked outside content
window.onclick = function(event) {
    if (event.target == modal) {
        modal.style.display = "none";
    }
}

// Switch Tabs Logic
function switchTab(tabName) {
    if .classList.remove("active");
        tabs[1].classList.add("active");
    }
}
</body>
</html>
