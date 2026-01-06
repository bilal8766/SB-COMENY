<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SB COMENY - Registration</title>
    <meta name="description" content="Register at SB COMENY - Create your account with email and mobile OTP verification.">
    
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        /* ========== HEADER / NAVBAR ========== */
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 30px;
            background: white;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        /* Logo - Left Side */
        .logo-section {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo {
            width: 60px;
            height: 60px;
        }
        
        .company-name {
            font-size: 1.8em;
            font-weight: bold;
            color: #333;
        }
        
        .company-name span {
            color: #ff416c;
        }
        
        /* Navigation - Right Side */
        .nav-links {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .nav-btn {
            padding: 10px 25px;
            border-radius: 25px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .nav-btn.home {
            background: transparent;
            color: #333;
            border-color: #ddd;
        }
        
        .nav-btn.home:hover {
            background: #f0f0f0;
            border-color: #ccc;
        }
        
        .nav-btn.login {
            background: transparent;
            color: #667eea;
            border-color: #667eea;
        }
        
        .nav-btn.login:hover {
            background: #667eea;
            color: white;
        }
        
        .nav-btn.register {
            background: linear-gradient(90deg, #ff416c, #ff4b2b);
            color: white;
            border-color: #ff416c;
        }
        
        .nav-btn.register:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(255, 65, 108, 0.4);
        }
        
        /* Mobile Menu Button */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            gap: 5px;
        }
        
        .menu-toggle span {
            width: 25px;
            height: 3px;
            background: #333;
            border-radius: 3px;
            transition: 0.3s;
        }
        
        /* ========== MAIN CONTENT ========== */
        .main-content {
            padding: 40px 20px;
            text-align: center;
        }
        
        .welcome-line {
            font-size: 1.5em;
            color: white;
            background: linear-gradient(90deg, #ff416c, #ff4b2b);
            padding: 15px 40px;
            margin: 20px auto;
            border-radius: 50px;
            display: inline-block;
            box-shadow: 0 4px 15px rgba(255, 65, 108, 0.4);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.02); }
        }
        
        h1 {
            color: white;
            font-size: 3em;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            margin: 20px 0;
        }
        
        .subtitle {
            font-size: 1.2em;
            color: rgba(255,255,255,0.9);
            max-width: 600px;
            margin: 0 auto 40px;
            line-height: 1.6;
        }
        
        /* ========== REGISTRATION FORM ========== */
        .registration-form {
            max-width: 450px;
            margin: 30px auto;
            padding: 40px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0,0,0,0.2);
            text-align: left;
        }
        
        .registration-form h2 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
            font-size: 1.8em;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #555;
            font-weight: 600;
        }
        
        .form-group input {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 1em;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);
        }
        
        .form-group input:disabled {
            background: #f5f5f5;
            cursor: not-allowed;
        }
        
        .phone-input-group {
            display: flex;
            gap: 10px;
        }
        
        .country-code {
            width: 80px !important;
            text-align: center;
        }
        
        .btn {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 10px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }
        
        .btn-otp {
            background: linear-gradient(90deg, #667eea, #764ba2);
            color: white;
            margin-top: 10px;
        }
        
        .btn-otp:hover:not(:disabled) {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.4);
        }
        
        .btn-verify {
            background: linear-gradient(90deg, #11998e, #38ef7d);
            color: white;
        }
        
        .btn-verify:hover:not(:disabled) {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(56, 239, 125, 0.4);
        }
        
        .btn-logout {
            background: linear-gradient(90deg, #ff416c, #ff4b2b);
            color: white;
        }
        
        .message {
            padding: 12px;
            border-radius: 10px;
            margin-bottom: 20px;
            text-align: center;
            display: none;
        }
        
        .message.success {
            background: #d4edda;
            color: #155724;
            display: block;
        }
        
        .message.error {
            background: #f8d7da;
            color: #721c24;
            display: block;
        }
        
        .otp-section {
            display: none;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 2px dashed #e0e0e0;
        }
        
        .otp-section.show {
            display: block;
        }
        
        #userInfo {
            display: none;
            text-align: center;
        }
        
        #userInfo h3 {
            color: #28a745;
            margin-bottom: 20px;
        }
        
        .user-avatar {
            width: 80px;
            height: 80px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 2em;
            color: white;
        }
        
        /* ========== PERSONAL DETAILS ========== */
        .personal-details {
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 40px auto;
            padding: 30px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0,0,0,0.2);
            max-width: 500px;
            gap: 25px;
            flex-wrap: wrap;
        }
        
        .photo {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid #667eea;
        }
        
        .details {
            text-align: left;
        }
        
        .details h2 {
            color: #333;
            margin-bottom: 15px;
        }
        
        .details p {
            margin: 8px 0;
            color: #666;
        }
        
        /* ========== RESPONSIVE ========== */
        @media (max-width: 768px) {
            .navbar {
                padding: 10px 15px;
            }
            
            .logo {
                width: 45px;
                height: 45px;
            }
            
            .company-name {
                font-size: 1.3em;
            }
            
            .nav-links {
                display: none;
                position: absolute;
                top: 70px;
                right: 15px;
                background: white;
                flex-direction: column;
                padding: 15px;
                border-radius: 10px;
                box-shadow: 0 5px 20px rgba(0,0,0,0.2);
                gap: 10px;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .menu-toggle {
                display: flex;
            }
            
            h1 {
                font-size: 2em;
            }
            
            .welcome-line {
                font-size: 1.1em;
                padding: 12px 25px;
            }
            
            .registration-form {
                margin: 20px 15px;
                padding: 25px 20px;
            }
        }
    </style>
</head>
<body>

    <!-- ========== NAVBAR ========== -->
    <nav class="navbar">
        <!-- Logo - LEFT SIDE -->
        <div class="logo-section">
            <svg class="logo" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="logoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" style="stop-color:#667eea"/>
                        <stop offset="100%" style="stop-color:#764ba2"/>
                    </linearGradient>
                </defs>
                <circle cx="100" cy="100" r="90" fill="url(#logoGradient)" stroke="white" stroke-width="5"/>
                <text x="100" y="90" font-family="Arial" font-size="50" font-weight="bold" fill="#ff416c" text-anchor="middle">SB</text>
                <text x="100" y="125" font-family="Arial" font-size="20" fill="white" text-anchor="middle">COMENY</text>
            </svg>
            <div class="company-name"><span>SB</span> COMENY</div>
        </div>
        
        <!-- Navigation Buttons - RIGHT SIDE -->
        <div class="nav-links" id="navLinks">
            <a href="#" class="nav-btn home">🏠 Home</a>
            <a href="#" class="nav-btn login">🔑 Login</a>
            <a href="#" class="nav-btn register">📝 Register</a>
        </div>
        
        <!-- Mobile Menu Toggle -->
        <div class="menu-toggle" onclick="toggleMenu()">
            <span></span>
            <span></span>
            <span></span>
        </div>
    </nav>

    <!-- ========== MAIN CONTENT ========== -->
    <div class="main-content">
        <div class="welcome-line">🎉 HELLO! WELCOME TO MY COMPANY 🎉</div>
        
        <h1>SB COMENY</h1>
        <p class="subtitle">Welcome to SB COMENY! This is the starting page of your dream company. We're just getting started—stay tuned for more amazing things!</p>
        
        <!-- Registration Form -->
        <div class="registration-form">
            <h2>📝 Create Account</h2>
            
            <div id="message" class="message"></div>
            
            <div id="registrationForm">
                <div class="form-group">
                    <label>👤 Full Name</label>
                    <input type="text" id="fullname" placeholder="Enter your full name" required>
                </div>
                
                <div class="form-group">
                    <label>📧 Email Address</label>
                    <input type="email" id="email" placeholder="example@email.com" required>
                </div>
                
                <div class="form-group">
                    <label>📱 Mobile Number</label>
                    <div class="phone-input-group">
                        <input type="text" id="countryCode" class="country-code" value="+91">
                        <input type="tel" id="mobile" placeholder="9876543210" maxlength="10" required>
                    </div>
                </div>
                
                <div id="recaptcha-container"></div>
                
                <button class="btn btn-otp" id="sendOtpBtn" onclick="sendOTP()">📤 Send OTP</button>
                
                <div class="otp-section" id="otpSection">
                    <div class="form-group">
                        <label>🔐 Enter OTP</label>
                        <input type="text" id="otp" placeholder="Enter 6-digit OTP" maxlength="6">
                    </div>
                    <button class
