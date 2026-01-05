<!Bilal Khan>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Welcome</title>
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
            padding: 0;
        }
        .navbar {
            background-color: #333;
            padding: 15px;
            text-align: right;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            margin: 0 5px;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            display: inline-block;
            cursor: pointer;
        }
        .navbar a:hover {
            background-color: #555;
        }
        .navbar .home-btn {
            background-color: #4CAF50;
        }
        .navbar .register-btn {
            background-color: #2196F3;
        }
        .navbar .login-btn {
            background-color: #FF9800;
        }
        .navbar .logout-btn {
            background-color: #f44336;
        }
        .logo {
            width: 200px;
            height: 200px;
            float: left;
            margin-right: 20px;
            margin-left: 20px;
        }
        .personal-details {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            max-width: 600px;
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
            margin: 20px 0;
        }
        p {
            font-size: 1.2em;
            color: #666;
            margin: 10px 0;
        }
        .welcome-line {
            font-size: 2em;
            color: white;
            background-color: red;
            padding: 15px;
            margin: 20px auto;
            max-width: 800px;
            border-radius: 5px;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        .clearfix::after {
            content: "";
            clear: both;
            display: table;
        }
        .form-section {
            background: white;
            padding: 30px;
            margin: 20px auto;
            max-width: 600px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .form-section h2 {
            margin-bottom: 20px;
        }
        .form-section input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .form-section button {
            width: 100%;
            padding: 10px;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 10px;
        }
        .register-btn-form {
            background-color: #2196F3;
        }
        .login-btn-form {
            background-color: #FF9800;
        }
        /* Profile Page Styles */
        .profile-section {
            background: white;
            padding: 40px;
            margin: 20px auto;
            max-width: 600px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .profile-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #4CAF50;
            margin-bottom: 20px;
        }
        .profile-name {
            font-size: 2em;
            color: #333;
            margin-bottom: 20px;
        }
        .profile-info {
            text-align: left;
            background: #f9f9f9;
            padding: 20px;
            border-radius: 10px;
        }
        .profile-info p {
            margin: 10px 0;
            font-size: 1.1em;
        }
        .logout-profile-btn {
            background-color: #f44336;
            color: white;
            padding: 10px 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 20px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <!-- नेविबार -->
    <nav class="navbar">
        <a href="#" class="home-btn" onclick="showHome()">Home</a>
        <a href="#register" class="register-btn" onclick="showRegister()">Register</a>
        <a href="#login" class="login-btn" onclick="showLogin()">Login</a>
        <a href="#logout" class="logout-btn hidden" onclick="logout()">Logout</a>
    </nav>

    <div class="container clearfix">
        <!-- होम पेज -->
        <div id="home-page">
            <!-- Custom SVG Logo for SB COMENY -->
            <svg class="logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <circle cx="100" cy="100" r="90" fill="#4CAF50" stroke="#333" stroke-width="5"/>
                <text x="100" y="90" font-family="Arial, sans-serif" font-size="50" font-weight="bold" fill="red" text-anchor="middle">SB</text>
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
        </div>

        <!-- रजिस्ट्रेशन सेक्शन -->
        <div id="register-section" class="form-section hidden">
            <h2 style="color: #2196F3;">Register</h2>
            <form onsubmit="registerUser(event)">
                <input type="text" id="reg-name" placeholder="Full Name" required>
                <input type="email" id="reg-email" placeholder="Email Address" required>
                <input type="password" id="reg-password" placeholder="Password" required>
                <input type="text" id="reg-photo" placeholder="Photo URL (optional)">
                <button type="submit" class="register-btn-form">Register Now</button>
            </form>
            <p style="margin-top: 15px;">Already have an account? <a href="#" onclick="showLogin()">Login here</a></p>
        </div>

        <!-- लॉगिन सेक्शन -->
        <div id="login-section" class="form-section hidden">
            <h2 style="color: #FF9800;">Login</h2>
            <form onsubmit="loginUser(event)">
                <input type="email" id="login-email" placeholder="Email Address" required>
                <input type="password" id="login-password" placeholder="Password" required>
                <button type="submit" class="login-btn-form">Login</button>
            </form>
            <p style="margin-top: 15px;">Don't have an account? <a href="#" onclick="showRegister()">Register here</a></p>
        </div>

        <!-- प्रोफाइल पेज -->
        <div id="profile-section" class="profile-section hidden">
            <h2 style="color: #4CAF50; margin-bottom: 20px;">My Profile</h2>
            <img id="profile-photo-img" src="" alt="Profile Photo" class="profile-photo">
            <h1 id="profile-name" class="profile-name"></h1>
            <div class="profile-info">
                <p><strong>Email:</strong> <span id="profile-email"></span></p>
                <p><strong>Member Since:</strong> <span id="profile-date"></span></p>
            </div>
            <button class="logout-profile-btn" onclick="logout()">Logout</button>
        </div>
    </div>

    <script>
        // पेज लोड होने पर चेक करें कि यूज़र लॉगिन है या नहीं
        document.addEventListener('DOMContentLoaded', function() {
            checkLogin();
        });

        // होम पेज दिखाएं
        function showHome() {
            document.getElementById('home-page').classList.remove('hidden');
            document.getElementById('register-section').classList.add('hidden');
            document.getElementById('login-section').classList.add('hidden');
            document.getElementById('profile-section').classList.add('hidden');
        }

        // रजिस्ट्रेशन पेज दिखाएं
        function showRegister() {
            document.getElementById('home-page').classList.add('hidden');
            document.getElementById('register-section').classList.remove('hidden');
            document.getElementById('login-section').classList.add('hidden');
            document.getElementById('profile-section').classList.add('hidden');
        }

        // लॉगिन पेज दिखाएं
        function showLogin() {
            document.getElementById('home-page').classList.add('hidden');
            document.getElementById('register-section').classList.add('hidden');
            document.getElementById('login-section').classList.remove('hidden');
            document.getElementById('profile-section').classList.add('hidden');
        }

        // प्रोफाइल पेज दिखाएं
        function showProfile() {
            document.getElementById('home-page').classList.add('hidden');
            document.getElementById('register-section').classList.add('hidden');
            document.getElementById('login-section').classList.add('hidden');
            document.getElementById('profile-section').classList.remove('hidden');
            
            // लॉगआउट बटन दिखाएं
            document.querySelector('.logout-btn').classList.remove('hidden');
            
            // यूज़र डेटा प्रोफाइल में दिखाएं
            const user = JSON.parse(localStorage.getItem('currentUser'));
            if (user) {
                document.getElementById('profile-name').textContent = user.name;
                document.getElementById('profile-email').textContent = user.email;
                document.getElementById('profile-date').textContent = user.registerDate;
                document.getElementById('profile-photo-img').src = user.photo || 'https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg';
            }
        }

        // रजिस्ट्रेशन फंक्शन
        function registerUser(event) {
            event.preventDefault();
            
            const name = document.getElementById('reg-name').value;
            const email = document.getElementById('reg-email').value;
            const password = document.getElementById('reg-password').value;
            const photo = document.getElementById('reg-photo').value;
            
            // यूज़र डेटा सेव करें
            const userData = {
                name: name,
                email: email,
                password: password,
                photo: photo,
                registerDate: new Date().toLocaleDateString()
            };
            
            localStorage.setItem('user_' + email, JSON.stringify(userData));
            
            alert('Registration successful! Please login.');
            showLogin();
        }

        // लॉगिन फंक्शन
        function loginUser(event) {
            event.preventDefault();
            
            const email = document.getElementById('login-email').value;
            const password = document.getElementById('login-password').value;
            
            // यूज़र डेटा चेक करें
            const storedUser = localStorage.getItem('user_' + email);
            
            if (storedUser) {
                const user = JSON.parse(storedUser);
                if (user.password === password) {
                    // लॉगिन सफल - करंट यूज़र सेट करें
                    localStorage.setItem('currentUser', JSON.stringify(user));
                    alert('Login successful! Welcome ' + user.name);
                    showProfile();
                    return;
                }
            }
            
            alert('Invalid email or password!');
        }

        // लॉगिन चेक करें
        function checkLogin() {
            const currentUser = localStorage.getItem('currentUser');
            if (currentUser) {
                showProfile();
                document.querySelector('.logout-btn').classList.remove('hidden');
            }
        }

        // लॉगआउट फंक्शन
        function logout() {
            localStorage.removeItem('currentUser');
            alert('Logged out successfully!');
            showHome();
            document.querySelector('.logout-btn').classList.add('hidden');
        }
    </script>
</body>
</html>
