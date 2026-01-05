<MOHD BILAL >
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Welcome</title>
    <meta name="description" content="Welcome to SB COMENY, your dream company from Haryana. Contact Mohd Bilal at 9813490892 or riyan.khan4712@gmail.com for more details.">
    <meta name="keywords" content="SB COMENY, company, Haryana, Mohd Bilal, business">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            margin: 0;
            padding: 50px;
        }
        .logo {
            width: 200px;
            height: 200px;
            float: right;
            margin-left: 20px;
        }
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 20px;
            background-color: #333;
            border-radius: 10px;
            margin-bottom: 20px;
        }
        .header h2 {
            color: white;
            margin: 0;
        }
        .header-buttons {
            display: flex;
            gap: 10px;
        }
        .register-btn, .login-btn {
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
            transition: background-color 0.3s;
        }
        .register-btn {
            background-color: #4CAF50;
        }
        .register-btn:hover {
            background-color: #45a049;
        }
        .login-btn {
            background-color: #2196F3;
        }
        .login-btn:hover {
            background-color: #0b7dda;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.5);
        }
        .modal-content {
            background-color: white;
            margin: 15% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 300px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.3);
        }
        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close:hover {
            color: black;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #333;
            text-align: left;
        }
        .form-group input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }
        .submit-btn {
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            font-size: 1em;
        }
        .register-submit {
            background-color: #4CAF50;
        }
        .register-submit:hover {
            background-color: #45a049;
        }
        .login-submit {
            background-color: #2196F3;
        }
        .login-submit:hover {
            background-color: #0b7dda;
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
            width: 100px;
            height: 100px;
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
        }
        .details p {
            margin: 5px 0;
            color: #666;
        }
        h1 {
            color: #333;
            font-size: 3em;
        }
        p {
            font-size: 1.2em;
            color: #666;
        }
        .welcome-line {
            font-size: 2em;
            color: white;
            background-color: red;
            padding: 10px;
            margin: 20px 0;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <!-- Header with Register and Login Buttons -->
    <div class="header">
        <h2>SB COMENY</h2>
        <div class="header-buttons">
            <button class="register-btn" onclick="openRegisterModal()">Register</button>
            <button class="login-btn" onclick="openLoginModal()">Login</button>
        </div>
    </div>

    <!-- Custom SVG Logo for SB COMENY -->
    <svg class="logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
        <!-- Background circle for a modern look -->
        <circle cx="100" cy="100" r="90" fill="#4CAF50" stroke="#333" stroke-width="5"/>
        <!-- "SB" initials in bold, now red -->
        <text x="100" y="90" font-family="Arial, sans-serif" font-size="50" font-weight="bold" fill="red" text-anchor="middle">SB</text>
        <!-- "COMENY" below -->
        <text x="100" y="120" font-family="Arial, sans-serif" font-size="18" fill="white" text-anchor="middle">COMENY</text>
    </svg>
    
    <div class="welcome-line">HELLO WELCOM MY COMPANY</div>
    
    <h1>SB COMENY</h1>
    <p>Welcome to SB COMENY! This is the starting page of your dream company. We're just getting started—stay tuned for more!</p>
    
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
    
    <!-- Registration Modal -->
    <div id="registerModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeRegisterModal()">&times;</span>
            <h2 style="text-align: center; color: #333;">Register</h2>
            <form>
                <div class="form-group">
                    <label for="fullname">Full Name:</label>
                    <input type="text" id="fullname" name="fullname" placeholder="Enter your full name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" placeholder="Enter your email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Phone Number:</label>
                    <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required>
                </div>
                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" placeholder="Create a password" required>
                </div>
                <button type="submit" class="submit-btn register-submit">Register Now</button>
            </form>
        </div>
    </div>

    <!-- Login Modal -->
    <div id="loginModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeLoginModal()">&times;</span>
            <h2 style="text-align: center; color: #333;">Login</h2>
            <form>
                <div class="form-group">
                    <label for="login-email">Email:</label>
                    <input type="email" id="login-email" name="login-email" placeholder="Enter your email" required>
                </div>
                <div class="form-group">
                    <label for="login-password">Password:</label>
                    <input type="password" id="login-password" name="login-password" placeholder="Enter your password" required>
                </div>
                <button type="submit" class="submit-btn login-submit">Login</button>
            </form>
        </div>
    </div>

    <script>
        // Get the modals
        var registerModal = document.getElementById("registerModal");
        var loginModal = document.getElementById("loginModal");

        // Functions to open the modals
        function openRegisterModal() {
            registerModal.style.display = "block";
            loginModal.style.display = "none";
        }

        function openLoginModal() {
            loginModal.style.display = "block";
            registerModal.style.display = "none";
        }

        // Functions to close the modals
        function closeRegisterModal() {
            registerModal.style.display = "none";
        }

        function closeLoginModal() {
            loginModal.style.display = "none";
        }

        // Close the modal when clicking outside of it
        window.onclick = function(event) {
            if (event.target == registerModal) {
                registerModal.style.display = "none";
            }
            if (event.target == loginModal) {
                loginModal.style.display = "none";
            }
        }
    </script>
</body>
</html>
