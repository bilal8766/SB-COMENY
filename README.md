<!MOHD BILAL >
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Welcome</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: Arial, sans-serif; text-align: center; background-color: #f0f0f0; }
        .navbar { background-color: #333; padding: 15px; text-align: right; }
        .navbar a { color: white; text-decoration: none; padding: 10px 20px; margin: 0 5px; border-radius: 5px; cursor: pointer; }
        .navbar .home-btn { background-color: #4CAF50; }
        .navbar .register-btn { background-color: #2196F3; }
        .navbar .login-btn { background-color: #FF9800; }
        .navbar .logout-btn { background-color: #f4436; }
        .logo { width: 200px; height: 200px; float: left; margin: 0 20px; }
        .personal-details { display: flex; align-items: center; justify-content: center; margin: 20px auto; padding: 20px; background: white; border-radius: 10px; max-width: 600px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .photo { width: 100px; height: 100px; border-radius: 50%; object-fit: cover; margin-right: 20px; }
        .details { text-align: left; }
        .details h2 { margin: 0 0 10px 0; color: #333; }
        .details p { margin: 5px 0; color: #666; }
        h1 { color: #333; font-size: 3em; margin: 20px 0; clear: both; }
        .welcome-line { font-size: 2em; color: white; background-color: red; padding: 15px; margin: 20px auto; max-width: 800px; border-radius: 5px; }
        .container { max-width: 1200px; margin: 0 auto; padding: 20px; }
        .form-section { background: white; padding: 30px; margin: 20px auto; max-width: 500px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .form-section input { width: 100%; padding: 12px; margin: 10px 0; border: 1px solid #ddd; border-radius: 5px; box-sizing: border-box; }
        .form-section button { width: 100%; padding: 12px; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; margin-top: 10px; }
        .register-btn-form { background-color: #2196F3; }
        .login-btn-form { background-color: #FF9800; }
        .profile-section { background: white; padding: 40px; margin: 20px auto; max-width: 600px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .profile-photo { width: 150px; height: 150px; border-radius: 50%; object-fit: cover; border: 5px solid #4CAF50; margin-bottom: 20px; }
        .profile-name { font-size: 2em; color: #333; margin-bottom: 20px; }
        .profile-info { text-align: left; background: #f9f9f9; padding: 20px; border-radius: 10px; }
        .profile-info p { margin: 10px 0; font-size: 1.1em; }
        .logout-profile-btn { background-color: #f4436; color: white; padding: 10px 30px; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; margin-top: 20px; }
        .hidden { display: none; }
        .forgot-link { display: block; margin-top: 10px; color: #2196F3; cursor: pointer; text-decoration: underline; }
        .alert { padding: 10px; margin-bottom: 15px; border-radius: 5px; }
        .alert-error { background: #ffebee; color: #c62828; }
        .alert-success { background: #e8f5e9; color: #2e7d32; }
    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#" class="home-btn" onclick="showHome()">Home</a>
        <a href="#register" class="register-btn" onclick="showRegister()">Register</a>
        <a href="#login" class="login-btn" onclick="showLogin()">Login</a>
        <a href="#logout" class="logout-btn hidden" onclick="logout()">Logout</a>
    </nav>

    <div class="container">
        <!-- Home Page -->
        <div id="home-page">
            <svg class="logo" viewBox="0 0 200 200">
                <circle cx="100" cy="100" r="90" fill="#4CAF50" stroke="#333" stroke-width="5"/>
                <text x="100" y="90" font-family="Arial" font-size="50" font-weight="bold" fill="red" text-anchor="middle">SB</text>
                <text x="100" y="120" font-family="Arial" font-size="18" fill="white" text-anchor="middle">COMENY</text>
            </svg>
            <div class="welcome-line">HELLO WELCOME MY COMPANY</div>
            <h1>SB COMENY</h1>
            <p>Welcome to SB COMENY!</p>
            <div class="personal-details">
                <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg" class="photo">
                <div class="details">
                    <h2>Mohd Bilal (Owner)</h2>
                    <p><strong>Mobile:</strong> +91 9813490892</p>
                    <p><strong>Email:</strong> riyan.khan4712@gmail.com</p>
                </div>
            </div>
        </div>

        <!-- Register Section -->
        <div id="register-section" class="form-section hidden">
            <h2 style="color: #2196F3;">Register</h2>
            <div id="reg-message"></div>
            <form onsubmit="registerUser(event)">
                <input type="text" id="reg-name" placeholder="Full Name" required>
                <input type="email" id="reg-email" placeholder="Email Address" required>
                <input type="password" id="reg-password" placeholder="Password" required>
                <input type="text" id="reg-photo" placeholder="Photo URL (Optional)">
                <button type="submit" class="register-btn-form">Register Now</button>
            </form>
            <p>Already have an account? <a href="#" onclick="showLogin()">Login here</a></p>
        </div>

        <!-- Login Section -->
        <div id="login-section" class="form-section hidden">
            <h2 style="color: #FF9800;">Login</h2>
            <div id="login-message"></div>
            <form onsubmit="loginUser(event)">
                <input type="email" id="login-email" placeholder="Email Address" required>
                <input type="password" id="login-password" placeholder="Password" required>
                <button type="submit" class="login-btn-form">Login</button>
            </form>
            <span class="forgot-link" onclick="showForgotPassword()">Forgot Password?</span>
            <p>Don't have an account? <a href="#" onclick="showRegister()">Register here</a></p>
        </div>

        <!-- Forgot Password Section -->
        <div id="forgot-password-section" class="form-section hidden">
            <h2 style="color: #f4436;">Forgot Password</h2>
            <p>Enter your email to receive reset link.</p>
            <div id="fp-message"></div>
            <form onsubmit="handleForgotPassword(event)">
                <input type="email" id="fp-email" placeholder="Enter your Email" required>
                <button type="submit" style="background-color: #f4436;">Send Reset Link</button>
            </form>
            <p onclick="showLogin()" style="cursor: pointer; margin-top: 15px; color: #666;">← Back to Login</p>
        </div>

        <!-- Profile Section -->
        <div id="profile-section" class="profile-section hidden">
            <h2 style="color: #4CAF50;">My Profile</h2>
            <img id="profile-photo-img" src="" class="profile-photo">
            <h1 id="profile-name" class="profile-name"></h1>
            <div class="profile-info">
                <p><strong>Email:</strong> <span id="profile-email"></span></p>
                <p><strong>Member Since:</strong> <span id="profile-date"></span></p>
            </div>
            <button class="logout-profile-btn" onclick="logout()">Logout</button>
        </div>
    </div>

    <script>
        const API_URL = 'http://localhost:3000/api';

        function showHome() { hideAll(); document.getElementById('home-page').classList.remove('hidden'); }
        function showRegister() { hideAll(); document.getElementById('register-section').classList.remove('hidden'); }
        function showLogin() { hideAll(); document.getElementById('login-section').classList.remove('hidden'); }
        function showForgotPassword() { hideAll(); document.getElementById('forgot-password-section').classList.remove('hidden'); }
        function hideAll() {
            ['home-page', 'register-section', 'login-section', 'forgot-password-section', 'profile-section'].forEach(id => document.getElementById(id).classList.add('hidden'));
        }

        function showMessage(elementId, message, type) {
            document.getElementById(elementId).innerHTML = `<div class="alert alert-${type}">${message}</div>`;
        }

        async function registerUser(event) {
            event.preventDefault();
            const name = document.getElementById('reg-name').value;
            const email = document.getElementById('reg-email').value;
            const password = document.getElementById('reg-password').value;
            const photo = document.getElementById('reg-photo').value;

            try {
                const response = await fetch(`${API_URL}/register`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ name, email, password, photo })
                });
                const data = await response.json();
                if (response.ok) { alert('Registration Successful!'); showLogin(); }
                else { showMessage('reg-message', data.message, 'error'); }
            } catch (error) { showMessage('reg-message', 'Server Error!', 'error'); }
        }

        async function loginUser(event) {
            event.preventDefault();
            const email = document.getElementById('login-email').value;
            const password = document.getElementById('login-password').value;

            try {
                const response = await fetch(`${API_URL}/login`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ email, password })
                });
                const data = await response.json();
                if (response.ok) { localStorage.setItem('sb_user', JSON.stringify(data.user)); showProfile(); }
                else { showMessage('login-message', data.message, 'error'); }
            } catch (error) { showMessage('login-message', 'Server Error!', 'error'); }
        }

        async function handleForgotPassword(event) {
            event.preventDefault();
            const email = document.getElementById('fp-email').value;
            try {
                const response = await fetch(`${API_URL}/forgot-password`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ email })
                });
                const data = await response.json();
                if (response.ok) { showMessage('fp-message', data.message, 'success'); alert('Check Server Console for Reset Link!'); }
                else { showMessage('fp-message', data.message, 'error'); }
            } catch (error) { showMessage('fp-message', 'Server Error!', 'error'); }
        }

        function showProfile() {
            hideAll();
            document.getElementById('profile-section').classList.remove('hidden');
            document.querySelector('.logout-btn').classList.remove('hidden');
            const user = JSON.parse(localStorage.getItem('sb_user'));
            if (user) {
                document.getElementById('profile-name').textContent = user.name;
                document.getElementById('profile-email').textContent = user.email;
                document.getElementById('profile-date').textContent = user.registerDate;
                document.getElementById('profile-photo-img').src = user.photo || 'https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg';
            }
        }

        function logout() {
            localStorage.removeItem('sb_user');
            alert('Logged out!');
            showHome();
            document.querySelector('.logout-btn').classList.add('hidden');
        }

        document.addEventListener('DOMContentLoaded', () => { if(localStorage.getItem('sb_user')) showProfile(); });
    </script>
</body>
</html>
