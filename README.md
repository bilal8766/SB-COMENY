<!MOHD BILAL html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Salt Products</title>
    <meta name="description" content="SB COMENY - Premium quality salt products. Contact Mohd Bilal at 9813490892 or riyan.khan4712@gmail.com for more details.">
    <meta name="keywords" content="SB COMENY, salt, namak, Haryana, Mohd Bilal, business">
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
            margin-right: 20px;
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
        
        h1 {
            color: #333;
            font-size: 2em;
            margin: 10px 0;
        }
        
        p {
            font-size: 1em;
            color: #666;
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
        
        .section-title {
            font-size: 1.5em;
            color: #333;
            margin: 20px 0;
        }
        
        /* Admin Panel Styles */
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
            max-width: 450px;
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
            margin-bottom: 12px;
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
        }
        
        .submit-btn:hover {
            background-color: #cc0000;
        }
        
        .loading {
            opacity: 0.7;
            pointer-events: none;
        }
        
        /* Responsive */
        @media (max-width: 600px) {
            .logo {
                width: 100px;
                height: 100px;
                float: none;
                margin: 0 auto 15px;
                display: block;
            }
            
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
            
            .orders-table {
                font-size: 0.8em;
            }
            
            .orders-table th, .orders-table td {
                padding: 8px;
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
    
    <div class="welcome-line">HELLO WELCOM MY COMPANY</div>
    
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
                    <div class="stat-label">Total Order </div>
                </div>
                <div class="stat-card green">
                    <div class="stat-number" id="completedOrders">0</div>
                    <div class="stat-label">पूर्ण ऑर्डर</div>
                </div>
                <div class="stat-card orange">
                    <div class="stat-number" id="pendingOrders">0</div>
                    <div class="stat-label">Pending Order</div>
                </div>
                <div class="stat-card red">
                    <div class="stat-number" id="totalRevenue">₹0</div>
                    <div class="stat-label">कुल कमाई</div>
                </div>
            </div>
            
            <!-- Filter Section -->
            <div class="filter-section">
                <input type="text" id="searchName" placeholder="Search Customer Name..." onkeyup="filterOrders()">
                <input type="text" id="searchProduct" placeholder="Search Product..." onkeyup="filterOrders()">
                <input type="date" id="filterDate" onchange="filterOrders()">
                <select id="filterStatus" onchange="filterOrders()">
                    <option value="all">All Status</option>
                    <option value="pending">Pending</option>
                    <option value="completed">पूर्ण</option>
                </select>
                <button onclick="filterOrders()">🔍 Search</button>
                <button onclick="exportOrders()">📥 एक्सपोर्ट</button>
                <button class="clear-all-btn" onclick="clearAllOrders()">🗑️ सभी हटाएं</button>
            </div>
            
            <!-- Orders Table -->
            <table class="orders-table">
                <thead>
                    <tr>
                        <th>Sr No</th>
                        <th>Date</th>
                        <th>Customer</th>
                        <th>प्रोडक्ट</th>
                        <th>मात्रा</th>
                        <th>कुल कीमत</th>
                        <th>फोन</th>
                        <th>पता</th>
                        <th>स्टेटस</th>
                        <th>एक्शन</th>
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
                    <input type="number" id="quantity" min="1" value="1" required>
                </div>
                
                <div class="form-group">
                    <label for="orderNotes">Additional Notes (Optional):</label>
                    <textarea id="orderNotes" placeholder="Any special instructions..."></textarea>
                </div>
                
                <button type="submit" class="submit-btn" id="submitBtn">Confirm Order</button>
            </form>
        </div>
    </div>
    
    <script>
        // Admin Password (You can change this)
        const ADMIN_PASSWORD = 'Bilal@3691';
        
        // Initialize orders from localStorage
        let orders = JSON.parse(localStorage.getItem('sbComenyOrders')) || [];
        
        // Open Admin Panel
        function openAdminPanel() {
            const password = prompt('🔐 Enter password to open Admin Panel:');
            
            if (password === ADMIN_PASSWORD) {
                document.getElementById('adminPanel').style.display = 'block';
                loadOrders();
            } else if (password !== null) {
                alert('❌ Wrong password!');
            }
        }
        
        // Close Admin Panel
        function closeAdminPanel() {
            document.getElementById('adminPanel').style.display = 'none';
        }
        
        // Load Orders to Table
        function loadOrders() {
            const tableBody = document.getElementById('ordersTableBody');
            tableBody.innerHTML = '';
            
            if (orders.length === 0) {
                tableBody.innerHTML = '<tr><td colspan="10" style="text-align:center; padding:20px;">No orders found yet!</td></tr>';
                updateStats();
                return;
            }
            
            // Sort by date (newest first)
            orders.sort((a, b) => new Date(b.date) - new Date(a.date));
            
            orders.forEach((order, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${index + 1}</td>
                    <td>${formatDate(order.date)}</td>
                    <td>${order.customerName}</td>
                    <td>${order.product}</td>
                    <td>${order.quantity}</td>
                    <td>₹${order.totalPrice}</td>
                    <td>${order.phone}</td>
                    <td>${order.address.substring(0, 30)}...</td>
                    <td><span class="status-badge ${order.status === 'completed' ? 'status-completed' : 'status-pending'}">${order.status === 'completed' ? 'Completed' : 'Pending'}</span></td>
                    <td>
                        <button class="action-btn btn-view" onclick="viewOrder(${index})">👁️</button>
                        ${order.status === 'pending' ? `<button class="action-btn btn-complete" onclick="markComplete(${index})">✓</button>` : ''}
                        <button class="action-btn btn-delete" onclick="deleteOrder(${index})">🗑️</button>
                    </td>
                `;
                tableBody.appendChild(row);
            });
            
            updateStats();
        }
        
        // Update Statistics
        function updateStats() {
            const totalOrders = orders.length;
            const completedOrders = orders.filter(o => o.status === 'completed').length;
            const pendingOrders = orders.filter(o => o.status === 'pending').length;
            const totalRevenue = orders
                .filter(o => o.status === 'completed')
                .reduce((sum, o) => sum + parseInt(o.totalPrice), 0);
            
            document.getElementById('totalOrders').textContent = totalOrders;
            document.getElementById('completedOrders').textContent = completedOrders;
            document.getElementById('pendingOrders').textContent = pendingOrders;
            document.getElementById('totalRevenue').textContent = '₹' + totalRevenue;
        }
        
        // Filter Orders
        function filterOrders() {
            const searchName = document.getElementById('searchName').value.toLowerCase();
            const searchProduct = document.getElementById('searchProduct').value.toLowerCase();
            const filterDate = document.getElementById('filterDate').value;
            const filterStatus = document.getElementById('filterStatus').value;
            
            const filteredOrders = orders.filter(order => {
                const matchesName = order.customerName.toLowerCase().includes(searchName);
                const matchesProduct = order.product.toLowerCase().includes(searchProduct);
                const matchesDate = !filterDate || order.date.startsWith(filterDate);
                const matchesStatus = filterStatus === 'all' || order.status === filterStatus;
                
                return matchesName && matchesProduct && matchesDate && matchesStatus;
            });
            
            const tableBody = document.getElementById('ordersTableBody');
            tableBody.innerHTML = '';
            
            if (filteredOrders.length === 0) {
                tableBody.innerHTML = '<tr><td colspan="10" style="text-align:center; padding:20px;">No orders found!</td></tr>';
                return;
            }
            
            filteredOrders.forEach((order, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${index + 1}</td>
                    <td>${formatDate(order.date)}</td>
                    <td>${order.customerName}</td>
                    <td>${order.product}</td>
                    <td>${order.quantity}</td>
                    <td>₹${order.totalPrice}</td>
                    <td>${order.phone}</td>
                    <td>${order.address.substring(0, 30)}...</td>
                    <td><span class="status-badge ${order.status === 'completed' ? 'status-completed' : 'status-pending'}">${order.status === 'completed' ? 'Completed' : 'Pending'}</span></td>
                    <td>
                        <button class="action-btn btn-view" onclick="viewOrder(${orders.indexOf(order)})">👁
                                                </button>
                        ${order.status === 'pending' ? `<button class="action-btn btn-complete" onclick="markComplete(${orders.indexOf(order)})">✓</button>` : ''}
                        <button class="action-btn btn-delete" onclick="deleteOrder(${orders.indexOf(order)})">🗑️</button>
                    </td>
                `;
                tableBody.appendChild(row);
            });
        }
        
        // Export Orders to CSV
        function exportOrders() {
            if (orders.length === 0) {
                alert('No orders to export!');
                return;
            }
            
            let csvContent = 'data:text/csv;charset=utf-8,';
            csvContent += 'Order No,Date,Customer Name,Product,Quantity,Total Price,Phone,Address,Status,Notes\n';
            
            orders.forEach((order, index) => {
                const row = [
                    index + 1,
                    formatDate(order.date),
                    order.customerName,
                    order.product,
                    order.quantity,
                    order.totalPrice,
                    order.phone,
                    order.address,
                    order.status,
                    order.notes || ''
                ].join(',');
                csvContent += row + '\n';
            });
            
            const encodedUri = encodeURI(csvContent);
            const link = document.createElement('a');
            link.setAttribute('href', encodedUri);
            link.setAttribute('download', 'sb_comeny_orders.csv');
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        }
        
        // Clear All Orders
        function clearAllOrders() {
            if (confirm('Are you sure you want to delete all orders? This action cannot be undone!')) {
                orders = [];
                saveOrders();
                loadOrders();
                alert('All orders have been deleted!');
            }
        }
        
        // View Order Details
        function viewOrder(index) {
            const order = orders[index];
            alert(
                `📋 ORDER DETAILS\n\n` +
                `Customer: ${order.customerName}\n` +
                `Phone: ${order.phone}\n` +
                `Address: ${order.address}\n` +
                `Product: ${order.product}\n` +
                `Quantity: ${order.quantity}\n` +
                `Total Price: ₹${order.totalPrice}\n` +
                `Date: ${formatDate(order.date)}\n` +
                `Status: ${order.status === 'completed' ? 'Completed' : 'Pending'}\n` +
                `Notes: ${order.notes || 'None'}`
            );
        }
        
        // Mark Order as Complete
        function markComplete(index) {
            if (confirm('Do you want to mark this order as completed?')) {
                orders[index].status = 'completed';
                saveOrders();
                loadOrders();
                alert('Order marked as completed!');
            }
        }
        
        // Delete Single Order
        function deleteOrder(index) {
            if (confirm('Do you want to delete this order?')) {
                orders.splice(index, 1);
                saveOrders();
                loadOrders();
                alert('Order deleted!');
            }
        }
        
        // Save Orders to localStorage
        function saveOrders() {
            localStorage.setItem('sbComenyOrders', JSON.stringify(orders));
        }
        
        // Format Date
        function formatDate(dateString) {
            const options = { year: 'numeric', month: 'short', day: 'numeric' };
            return new Date(dateString).toLocaleDateString('en-US', options);
        }
        
        // Open Order Modal
        function openOrderModal(productName, productPrice) {
            document.getElementById('productName').value = productName;
            document.getElementById('productPrice').value = productPrice;
            document.getElementById('orderModal').style.display = 'block';
        }
        
        // Close Order Modal
        function closeOrderModal() {
            document.getElementById('orderModal').style.display = 'none';
            document.getElementById('orderForm').reset();
        }
        
        // Submit Order
        function submitOrder(event) {
            event.preventDefault();
            
            const submitBtn = document.getElementById('submitBtn');
            submitBtn.textContent = '⏳ Submitting...';
            submitBtn.classList.add('loading');
            
            const productName = document.getElementById('productName').value;
            const productPrice = parseInt(document.getElementById('productPrice').value);
            const quantity = parseInt(document.getElementById('quantity').value);
            const totalPrice = productPrice * quantity;
            
            const order = {
                date: new Date().toISOString(),
                customerName: document.getElementById('customerName').value,
                phone: document.getElementById('customerPhone').value,
                address: document.getElementById('customerAddress').value,
                product: productName,
                quantity: quantity,
                totalPrice: totalPrice,
                status: 'pending',
                notes: document.getElementById('orderNotes').value
            };
            
            // Simulate network delay for better UX
            setTimeout(() => {
                orders.push(order);
                saveOrders();
                
                submitBtn.textContent = '✓ Order Placed!';
                submitBtn.style.backgroundColor = '#4CAF50';
                
                setTimeout(() => {
                    closeOrderModal();
                    submitBtn.textContent = 'Confirm Order';
                    submitBtn.classList.remove('loading');
                    submitBtn.style.backgroundColor = 'red';
                    alert('🎉 Thank you! Your order has been placed successfully. We will contact you soon.');
                }, 1000);
            }, 800);
        }
        
        // Close modal when clicking outside
        window.onclick = function(event) {
            const adminPanel = document.getElementById('adminPanel');
            const orderModal = document.getElementById('orderModal');
            
            if (event.target === adminPanel) {
                closeAdminPanel();
            }
            
            if (event.target === orderModal) {
                closeOrderModal();
            }
        };
        
        // Auto-refresh orders every 30 seconds
        setInterval(() => {
            if (document.getElementById('adminPanel').style.display === 'block') {
                loadOrders();
            }
        }, 30000);
    </script>
</body>
</html>
