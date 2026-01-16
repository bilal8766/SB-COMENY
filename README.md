<SINGARYA>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>SB COMENY • Secure Service Portal</title>
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet" />
<style>
  /* All your previously given CSS here */
  * {box-sizing: border-box;}
  body { margin:0; font-family:Poppins; min-height:100vh; background:linear-gradient(120deg,#5f2c82,#49a09d); color:#fff; }
  .header { padding:15px 30px; display:flex; justify-content:space-between; align-items:center; }
  .brand { font-size:22px; font-weight:700; }
  .brand span { color:#ff4b2b; }
  .topBtns { display:flex; gap:10px;}
  .topBtns button { padding:8px 16px; border:none; border-radius:6px; font-weight:600; color:#fff; cursor:pointer;}
  .loginBtn {background:#ff4b2b;}
  .regBtn {background:#0d6efd;}
  .adminBtn {background:#e91e63; padding:8px 12px;}
  .empBtn {background:#25D366;}
  .helpBtn {background:#ffc107; color:#000;}
  .main { display:flex; justify-content:center; gap:40px; padding:40px;}
  .profileCard { width:280px; background:rgba(255,255,255,.15); border-radius:20px; padding:25px; text-align:center;}
  .profileCard img { width:120px; height:120px; border-radius:50%; border:4px solid #fff; object-fit:cover;}
  .profileCard h3 { margin:15px 0 5px;}
  .profileCard p { margin:5px 0; font-size:14px;}
  .card { width:420px; background:rgba(255,255,255,.15); border-radius:20px; padding:30px;}
  .card h2 { text-align:center; margin-bottom:20px;}
  input {width:100%; padding:12px; margin:10px 0; border:none; border-radius:8px;}
  .btnMain { width:100%; padding:12px; border:none; border-radius:8px; background:#ff4b2b; color:#fff; font-weight:600; cursor:pointer;}
  .link { text-align:center; margin-top:10px; cursor:pointer; font-size:14px;}
  .hidden { display:none;}
  .tableWrap { max-height:260px; overflow:auto; background:rgba(255,255,255,.10); border-radius:12px; padding:10px;}
  table { width:100%; border-collapse:collapse; color:#fff; font-size:13px;}
  th,td { padding:8px; border-bottom:1px solid rgba(255,255,255,.2); text-align:left;}
  small { opacity:.85;}
  .modal { position:fixed; inset:0; background:rgba(0,0,0,.9); display:none; align-items:center; justify-content:center; flex-direction:column; z-index:999;}
  .modal img { max-width:90%; max-height:80%; border-radius:12px; border:3px solid #fff;}
  .modal button { margin-top:20px; padding:10px 20px; border:none; border-radius:6px; background:#ff4b2b; color:#fff; cursor:pointer;}
</style>
</head>
<body>

<div class="header">
  <div class="brand">SB <span>COMENY</span></div>
  <div class="topBtns">
    <button class="loginBtn" onclick="showLogin()">Login</button>
    <button class="regBtn" onclick="showRegister()">Register</button>
    <button class="adminBtn" onclick="goToAdminDashboard()">Admin</button>
    <button class="empBtn" onclick="openEmployee()">Employee</button>
    <button class="helpBtn" onclick="openHelp()">Help</button>
  </div>
</div>

<div class="main">
  <div class="profileCard">
    <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg" alt="Owner Image" />
    <h3>MOHD BILAL</h3>
    <p>Owner</p>
    <p>📞 9813490892</p>
  </div>

  <div class="card">
    <div id="loginBox">
      <h2>Login</h2>
      <input id="lUser" placeholder="Email or Username" />
      <input id="lPass" type="password" placeholder="Password" />
      <button class="btnMain" onclick="login()">Login</button>
      <div class="link" onclick="showRegister()">Create Account</div>
    </div>

    <div id="registerBox" class="hidden">
      <h2>Register</h2>
      <input id="rName" placeholder="Full Name" />
      <input id="rUser" placeholder="Username" />
      <input id="rEmail" placeholder="Email" />
      <input id="rPass" type="password" placeholder="Password" />
      <button class="btnMain" onclick="register()">Register</button>
      <div class="link" onclick="showLogin()">Back to Login</div>
    </div>

    <div id="dashBox" class="hidden">
      <h2 id="welcomeText"></h2>
      <div id="adminPanel" class="hidden" style="margin-top: 15px;">
        <h3 style="margin: 10px 0">Registered Users (Latest First)</h3>
        <div class="tableWrap">
          <table>
            <thead>
              <tr><th>Name</th><th>Username</th><th>Email</th><th>Created</th></tr>
            </thead>
            <tbody id="usersTbody"></tbody>
          </table>
        </div>
      </div>
      <button class="btnMain" onclick="logout()">Logout</button>
    </div>
  </div>
</div>

<div class="modal" id="empModal">
  <img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/naseem.jpeg" alt="Founder Image" />
  <h3>Naseem Khan – Founder</h3>
  <button onclick="closeEmployee()">Close</button>
</div>

<div class="modal" id="helpModal">
  <div style="width:min(520px,92vw);background:rgba(255,255,255,.12);padding:18px;border-radius:14px; color:#000;">
    <h2 style="margin:0 0 10px;">Help</h2>
    <p>Support Number: <b>9813490892</b></p>
    <button class="btnMain" style="background:#25D366;color:#fff;" onclick="window.open('https://wa.me/919813490892','_blank')">WhatsApp</button>
    <button style="margin-top:10px;background:#ff4b2b;" class="btnMain" onclick="closeHelp()">Close</button>
  </div>
</div>

<script type="module">
  // Firebase imports for app, auth, and firestore
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-app.js";
  import {
    getAuth,
    createUserWithEmailAndPassword,
    signInWithEmailAndPassword,
    onAuthStateChanged,
    signOut
  } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-auth.js";
  import {
    getFirestore,
    doc,
    setDoc,
    getDoc,
    runTransaction,
    collection,
    getDocs,
    query,
    orderBy,
    serverTimestamp
  } from "https://www.gstatic.com/firebasejs/10.12.5/firebase-firestore.js";

  // Your Firebase config
  const firebaseConfig = {
    apiKey: "AIzaSyB4MgojTiFnORRy8R04V0PrTDCdhAtX4f0",
    authDomain: "sb-comeny-4b868.firebaseapp.com",
    databaseURL: "https://sb-comeny-4b868-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "sb-comeny-4b868",
    storageBucket: "sb-comeny-4b868.firebasestorage.app",
    messagingSenderId: "738742516854",
    appId: "1:738742516854:web:42746572331fbac196b357",
    measurementId: "G-WGXV9ERTE3"
  };

  // Admin user UID (replace with your admin's actual UID)
  const ADMIN_UID = "AjsV5wAezsTIyzutmensvtqvHGR2";

  const app = initializeApp(firebaseConfig);
  const auth = getAuth(app);
  const db = getFirestore(app);

  // DOM elements selectors
  const loginBox = document.getElementById("loginBox");
  const registerBox = document.getElementById("registerBox");
  const dashBox = document.getElementById("dashBox");
  const welcomeText = document.getElementById("welcomeText");
  const adminPanel = document.getElementById("adminPanel");
  const usersTbody = document.getElementById("usersTbody");

  const lUser = document.getElementById("lUser");
  const lPass = document.getElementById("lPass");
  const rName = document.getElementById("rName");
  const rUser = document.getElementById("rUser");
  const rEmail = document.getElementById("rEmail");
  const rPass = document.getElementById("rPass");

  // Show login form
  window.showLogin = () => {
    loginBox.classList.remove("hidden");
    registerBox.classList.add("hidden");
    dashBox.classList.add("hidden");
    adminPanel.classList.add("hidden");
  };

  // Show register form
  window.showRegister = () => {
    loginBox.classList.add("hidden");
    registerBox.classList.remove("hidden");
    dashBox.classList.add("hidden");
    adminPanel.classList.add("hidden");
  };

  // Open employee modal
  window.openEmployee = () => {
    document.getElementById("empModal").style.display = "flex";
  };

  // Close employee modal
  window.closeEmployee = () => {
    document.getElementById("empModal").style.display = "none";
  };

  // Open help modal
  window.openHelp = () => {
    document.getElementById("helpModal").style.display = "flex";
  };

  // Close help modal
  window.closeHelp = () => {
    document.getElementById("helpModal").style.display = "none";
  };

  // Logout function
  window.logout = async () => {
    await signOut(auth);
    showLogin();
  };

  // Register function with username uniqueness enforced via Firestore transaction
  window.register = async () => {
    const name = rName.value.trim();
    const usernameRaw = rUser.value.trim();
    const email = rEmail.value.trim();
    const pass = rPass.value.trim();

    if (!name || !usernameRaw || !email || !pass) {
      alert("Please fill all fields.");
      return;
    }

    const username = usernameRaw.toLowerCase();

    try {
      const cred = await createUserWithEmailAndPassword(auth, email, pass);

      await runTransaction(db, async (tx) => {
        const usernameRef = doc(db, "usernames", username);
        const usernameSnap = await tx.get(usernameRef);

        if (usernameSnap.exists()) {
          throw new Error("Username already taken. Please choose another.");
        }

        tx.set(doc(db, "users", cred.user.uid), {
          name,
          username: usernameRaw,
          usernameLower: username,
          email,
          createdAt: serverTimestamp()
        });

        tx.set(usernameRef, {
          uid: cred.user.uid,
          email,
          createdAt: serverTimestamp()
        });
      });

      alert("Registered successfully!");
      showLogin();
    } catch (err) {
      alert(err.message);
    }
  };

  // Login function supports email or username
  window.login = async () => {
    const input = lUser.value.trim();
    const pass = lPass.value.trim();

    if (!input || !pass) {
      alert("Please enter Email/Username and Password.");
      return;
    }

    try {
      let emailToUse = input;

      if (!input.includes("@")) {
        const username = input.toLowerCase();
        const snap = await getDoc(doc(db, "usernames", username));

        if (!snap.exists()) {
          alert("Username not found.");
          return;
        }

        emailToUse = snap.data().email;
      }

      await signInWithEmailAndPassword(auth, emailToUse, pass);
    } catch (err) {
      alert("Login failed: " + err.message);
    }
  };

  // Load all registered users in admin dashboard
  async function loadAllUsersForAdmin() {
    usersTbody.innerHTML = `<tr><td colspan="4">Loading...</td></tr>`;

    const q = query(collection(db, "users"), orderBy("createdAt", "desc"));
    const snap = await getDocs(q);

    if (snap.empty) {
      usersTbody.innerHTML = `<tr><td colspan="4">No registered users found.</td></tr>`;
      return;
    }

    usersTbody.innerHTML = "";
    snap.forEach((docSnap) => {
      const u = docSnap.data();
      const created = u.createdAt?.toDate ? u.createdAt.toDate().toLocaleString() : "-";

      const tr = document.createElement("tr");
      tr.innerHTML = `<td>${u.name || "-"}</td><td>${u.username || "-"}</td><td>${u.email || "-"}</td><td>${created}</td>`;
      usersTbody.appendChild(tr);
    });
  }

  // Monitor auth state and show dashboard or login
  onAuthStateChanged(auth, async (user) => {
    if (!user) {
      adminPanel.classList.add("hidden");
      dashBox.classList.add("hidden");
      showLogin();
      return;
    }

    loginBox.classList.add("hidden");
    registerBox.classList.add("hidden");
    dashBox.classList.remove("hidden");

    if (user.uid === ADMIN_UID) {
      welcomeText.innerText = "Admin Dashboard";
      adminPanel.classList.remove("hidden");
      await loadAllUsersForAdmin();
    } else {
      welcomeText.innerText = "Welcome " + (user.email || "");
      adminPanel.classList.add("hidden");
    }
  });

  // Admin button logic: open dashboard if admin logged in, else prompt login
  window.goToAdminDashboard = async () => {
    const user = auth.currentUser;
    if (!user) {
      alert("Please login first with Admin credentials.");
      showLogin();
      return;
    }
    if (user.uid === ADMIN_UID) {
      adminPanel.classList.remove("hidden");
      dashBox.classList.remove("hidden");
      loginBox.classList.add("hidden");
      registerBox.classList.add("hidden");
      welcomeText.innerText = "Admin Dashboard";
      await loadAllUsersForAdmin();
      alert("Welcome Admin, Dashboard opened.");
    } else {
      alert("You are not authorized as admin.");
    }
  };
</script>

</body>
</html>
