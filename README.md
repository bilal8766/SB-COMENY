<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Registration</title>
    <meta name="description" content="Register at SB COMENY - Create your account with email and mobile OTP verification.">
    <meta name="keywords" content="SB COMENY, registration, signup, account">
    
    <!-- Firebase SDK Scripts -->
    <script type="module" src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app.js"></script>
    <script type="module" src="https://www.gstatic.com/firebasejs/10.7.1/firebase-auth.js"></script>
    
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
        .registration-form {
            max-width: 400px;
            margin: 20px auto;
            padding: 30px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            text-align: left;
        }
        .registration-form h2 {
            text-align: center;
            color: #333;
            margin-bottom: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #333;
            font-weight: bold;
        }
        .form-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1em;
            box-sizing: border-box;
        }
        .btn {
            width: 100%;
            padding: 12px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
            margin-top: 10px;
        }
        .btn:hover {
            background-color: #45a049;
        }
        .btn-otp {
            background-color: #2196F3;
        }
        .btn-otp:hover {
            background-color: #0b7dda;
        }
        .btn-logout {
            background-color: #f44336;
        }
        .btn-logout:hover {
            background-color: #da190b;
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
        .success-message {
            background-color: #d4edda;
            color: #155724;
            padding: 10px;
            border-radius: 5px;
            margin-bottom: 15px;
            text-align: center;
        }
        .error-message {
            background-color: #f8d7da;
            color: #721c24;
            padding: 10px;
            border-radius: 5px;
            margin-bottom: 15px;
            text-align: center;
        }
        #userInfo {
            display: none;
            background-color: #d4edda;
            padding: 20px;
            border-radius: 10px;
            max-width: 400px;
            margin: 20px auto;
        }
        #registrationForm {
            display: block;
        }
    </style>
</head>
<body>
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
    
    <!-- Registration Form Section -->
    <div class="registration-form">
        <h2>Create Account</h2>
        
        <div id="message"></div>
        
        <form id="registrationForm">
            <div class="form-group">
                <label for="fullname">Full Name:</label>
                <input type="text" id="fullname" name="fullname" placeholder="Enter your full name" required>
            </div>
            
            <div class="form-group">
                <label for="email">Email ID:</label>
                <input type="email" id="email" name="email" placeholder="Enter your email" required>
            </div>
            
            <div class="form-group">
                <label for="mobile">Mobile Number:</label>
                <input type="tel" id="mobile" name="mobile" placeholder="+91 9876543210" required>
            </div>
            
            <button type="button" class="btn btn-otp" id="sendOtpBtn" onclick="sendOTP()">Send OTP</button>
            
            <div class="form-group" style="margin-top: 15px;">
                <label for="otp">Enter OTP:</label>
                <input type="text" id="otp" name="otp" placeholder="Enter OTP received on mobile" disabled>
            </div>
            
            <button type="button" class="btn" onclick="verifyOTP()">Create Account</button>
        </form>
        
        <!-- Logged in user info -->
        <div id="userInfo">
            <h3>✅ Account Created Successfully!</h3>
            <p><strong>Name:</strong> <span id="userName"></span></p>
            <p><strong>Email:</strong> <span id="userEmail"></span></p>
            <p><strong>Phone:</strong> <span id="userPhone"></span></p>
            <button class="btn btn-logout" onclick="logout()">Logout</button>
        </div>
    </div>
    
    <!-- Personal Details Section -->
    <div class="personal-details">
        <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg" alt="Mohd Bilal Profile Picture" class="photo">
        <div class="details">
            <h2>Mohd Bilal</h2>
            <p><strong>Mobile:</strong> +91 1268315526</p>
            <p><strong>Email:</strong> riyan.khan4712@gmail.com</p>
            <p><strong>Facebook:</strong> MOHD BILAL</p>
        </div>
    </div>
    
    <script type="module">
        // Firebase Configuration - अपना Config यहाँ पेस्ट करें
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-app.js";
        import { getAuth, signInWithPhoneNumber, RecaptchaVerifier, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/10.7.1/firebase-auth.js";

        // ⚠️ अपना Firebase Config यहाँ पेस्ट करें:
        const firebaseConfig = {
            apiKey: "YOUR_API_KEY_HERE",
            authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
            projectId: "YOUR_PROJECT_ID",
            storageBucket: "YOUR_PROJECT_ID.appspot.com",
            messagingSenderId: "YOUR_SENDER_ID",
            appId: "YOUR_APP_ID"
        };

        // Firebase Initialize करें
        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        
        // OTP Send करने का फंक्शन
        window.sendOTP = async function() {
            const mobile = document.getElementById('mobile').value;
            const messageDiv = document.getElementById('message');
            
            if(mobile.length < 10) {
                messageDiv.innerHTML = '<div class="error-message">कृपया सही मोबाइल नंबर दर्ज करें!</div>';
                return;
            }
            
            try {
                // RecaptchaVerifier सेटअप
                window.recaptchaVerifier = new RecaptchaVerifier(auth, 'sendOtpBtn', {
                    'size': 'invisible',
                    'callback': (response) => {
                        // reCAPTCHA solved
                    }
                });
                
                const phoneNumber = mobile;
                const confirmationResult = await signInWithPhoneNumber(auth, phoneNumber, window.recaptchaVerifier);
                
                window.confirmationResult = confirmationResult;
                
                document.getElementById('otp').disabled = false;
                messageDiv.innerHTML = '<div class="success-message">OTP भेजा गया! कृपया अपने मोबाइल पर आए OTP दर्ज करें।</div>';
                
            } catch (error) {
                console.error("OTP Error:", error);
                messageDiv.innerHTML = '<div class="error-message">Error: ' + error.message + '</div>';
            }
        }
        
        // OTP Verify करने का फंक्शन
        window.verifyOTP = async function() {
            const otp = document.getElementById('otp').value;
            const messageDiv = document.getElementById('message');
            
            try {
                const result = await window.confirmationResult.confirm(otp);
                const user = result.user;
                
                // User info दिखाएँ
                document.getElementById('registrationForm').style.display = 'none';
                document.getElementById('userInfo').style.display = 'block';
                document.getElementById('userName').textContent = document.getElementById('fullname').value;
                document.getElementById('userEmail').textContent = document.getElementById('email').value;
                document.getElementById('userPhone').textContent = document.getElementById('mobile').value;
                
            } catch (error) {
                console.error("Verification Error:", error);
                messageDiv.innerHTML = '<div class="error-message">गलत OTP! कृपया सही OTP दर्ज करें।</div>';
            }
        }
        
        // Logout फंक्शन
        window.logout = async function() {
            await auth.signOut();
            document.getElementById('registrationForm').style.display = 'block';
            document.getElementById('userInfo').style.display = 'none';
            document.getElementById('otp').disabled = true;
            document.getElementById('otp').value = '';
            document.getElementById('message').innerHTML = '';
        }
        
        // Check if user is already logged in
        onAuthStateChanged(auth, (user) => {
            if (user) {
                document.getElementById('registrationForm').style.display = 'none';
                document.getElementById('userInfo').style.display = 'block';
            }
        });
    </script>
</body>
</html>
