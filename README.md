<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SB COMENY - Modern Admin Dashboard</title>
<style>
/* ===== GLOBAL ===== */
body{margin:0;font-family:'Segoe UI',Arial,sans-serif;background: linear-gradient(120deg,#667eea,#764ba2);transition: all 0.3s ease;}
header{text-align:center;font-size:2.2em;font-weight:900;color:white;padding:25px 0;background:linear-gradient(90deg,#ff416c,#ff4b2b);box-shadow:0 5px 25px rgba(0,0,0,.25);border-bottom-left-radius:20px;border-bottom-right-radius:20px;animation: pulse 2s infinite;}
@keyframes pulse{0%,100%{transform:scale(1);}50%{transform:scale(1.02);}}
header span{font-size:1.5em;margin-left:10px;}
.container{display:flex;gap:30px;flex-wrap:wrap;width:95%;max-width:1200px;justify-content:center;margin-top:30px;}
.left{width:260px;background:rgba(255,255,255,0.95);padding:25px;border-radius:20px;box-shadow:0 20px 50px rgba(0,0,0,.25);text-align:center;flex-shrink:0;transition: transform 0.3s;}
.left:hover{transform:translateY(-5px);}
.left img{width:120px;height:120px;border-radius:50%;border:5px solid #667eea;object-fit:cover;}
.left h3{margin:15px 0 5px;color:#333;}
.left p{margin:5px 0;font-weight:600;color:#555;}
.btn{width:100%;padding:12px;margin-top:10px;border:none;border-radius:12px;font-weight:700;cursor:pointer;transition:.25s;font-size:1em;}
.whatsapp{background:#25D366;color:#fff;}
.call{background:#0d6efd;color:#fff;}
.admin{background:linear-gradient(90deg,#ff416c,#ff4b2b);color:#fff;}
.btn:hover{transform:translateY(-2px);box-shadow:0 8px 20px rgba(0,0,0,.25);}
.main{flex:1;min-width:320px;max-width:700px;}
.card{background:rgba(255,255,255,0.95);padding:30px;border-radius:20px;box-shadow:0 20px 50px rgba(0,0,0,.25);margin-bottom:25px;transition:transform 0.3s;}
.card:hover{transform:translateY(-5px);}
.card h3{text-align:center;margin-bottom:20px;color:#333;font-size:1.8em;}
input,select{width:100%;padding:12px 14px;margin:10px 0;border-radius:12px;border:2px solid #ddd;font-size:1em;transition: all 0.3s;}
input:focus,select:focus{outline:none;border-color:#667eea;box-shadow:0 0 12px rgba(102,126,234,.3);}
.hidden{display:none;}
.modal-bg{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.6);display:flex;justify-content:center;align-items:center;z-index:999;display:none;}
.modal-content{background:#fff;padding:30px;border-radius:20px;width:90%;max-width:450px;box-shadow:0 20px 50px rgba(0,0,0,.3);}
.modal-content h3{text-align:center;margin-bottom:20px;}
.modal-content input{margin:10px 0;}
table{width:100%;border-collapse:collapse;background:#fff;border-radius:12px;overflow:hidden;}
th,td{padding:10px;border:1px solid #ddd;text-align:center;}
th{background:#667eea;color:#fff;cursor:pointer;}
th:hover{background:#5a67d8;}
</style>
</head>
<body>

<header>HELLO! WELCOME MY COMPANY <span>💔</span></header>

<div class="container">
<div class="left">
<img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg">
<h3>MOHD BILAL</h3>
<p>9813490892</p>
<p>(OWNER)</p>
<button class="btn whatsapp" onclick="window.open('https://wa.me/919813490892')">WhatsApp</button>
<button class="btn call" onclick="location.href='tel:9813490892'">Call</button>
<button class="btn admin" onclick="openAdmin()">ADMIN</button>
</div>

<div class="main">
<!-- MODAL FOR REGISTRATION -->
<div class="modal-bg" id="regModal">
<div class="modal-content">
<h3>Register</h3>
<input id="rName" placeholder="Full Name">
<input id="rMobile" placeholder="Mobile">
<input id="rEmail" placeholder="Email">
<input id="rUser" placeholder="Username">
<input id="rPass" type="password" placeholder="Password">
<button class="btn admin" onclick="register()">Register</button>
<button class="btn" onclick="closeModal()">Cancel</button>
</div>
</div>

<!-- LOGIN CARD -->
<div class="card" id="loginBox">
<h3>Login</h3>
<input id="loginUser" placeholder="Username">
<input id="loginPass" type="password" placeholder="Password">
<button class="btn admin" onclick="login()">Login</button>
<p style="text-align:center;cursor:pointer;margin-top:10px" onclick="openModal()">Register</p>
</div>

<!-- USER PROFILE -->
<div class="card hidden" id="userPage">
<h3>User Profile</h3>
<div id="userInfo" style="text-align:center;font-weight:600;"></div>
<button class="btn" onclick="alert('Help: 9813490892')">Help</button>
<button class="btn">Apply PAN Card</button>
<button class="btn">Aadhaar Address Change</button>
<button class="btn admin" onclick="logout()">Logout</button>
</div>

<!-- ADMIN DASHBOARD -->
<div class="card hidden" id="adminPage">
<h3>Admin Dashboard</h3>
<input id="searchUser" placeholder="Search Username..." onkeyup="filterUsers()">
<button class="btn" onclick="exportCSV()">Export CSV</button>
<table>
<thead>
<tr>
<th>Name</th>
<th>Username</th>
<th>Mobile</th>
<th>Status</th>
<th>Action</th>
</tr>
</thead>
<tbody id="adminData"></tbody>
</table>
</div>

</div>
</div>

<script type="module">
import { initializeApp } from "https://www.gstatic.com/firebasejs/9.22.1/firebase-app.js";
import { getDatabase, ref, push, set, onValue, update } from "https://www.gstatic.com/firebasejs/9.22.1/firebase-database.js";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT_ID.firebaseio.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
const db = getDatabase(app);

const ADMIN_PASS="Bilal@8990@3691@9813490892";

function openModal(){document.getElementById("regModal").style.display="flex";}
function closeModal(){document.getElementById("regModal").style.display="none";}
function validateEmail(email){return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);}

window.register = function(){
  let name=rName.value.trim();
  let mobile=rMobile.value.trim();
  let email=rEmail.value.trim();
  let user=rUser.value.trim();
  let pass=rPass.value.trim();

  if(!name||!mobile||!email||!user||!pass){alert("All fields required");return;}
  if(!/^\d{10}$/.test(mobile)){alert("Mobile must be 10 digits");return;}
  if(!validateEmail(email)){alert("Enter valid email");return;}
  if(pass.length<6){alert("Password min 6 char");return;}

  const usersRef = ref(db, 'users');
  const newUserRef = push(usersRef);
  set(newUserRef, {name,mobile,email,user,pass,active:true})
    .then(()=>{alert("Registered Successfully"); closeModal();})
    .catch(err=>alert("Error: "+err));
}

window.login = function(){
  const usersRef = ref(db, 'users');
  const username = loginUser.value;
  const password = loginPass.value;
  onValue(usersRef, snapshot=>{
    const users = snapshot.val();
    let found = false;
    for(let key in users){
      const u = users[key];
      if(u.user===username && u.pass===password){
        found = true;
        if(!u.active){alert("Account Deactivated"); return;}
        document.getElementById("loginBox").classList.add("hidden");
        document.getElementById("userPage").classList.remove("hidden");
        userInfo.innerHTML=`<b>Name:</b> ${u.name}<br><b>Mobile:</b> ${u.mobile}<br><b>Email:</b> ${u.email}`;
      }
    }
    if(!found) alert("Wrong login");
  }, {onlyOnce:true});
}

window.logout = function(){location.reload();}

window.openAdmin = function(){
  let p = prompt("Admin Password");
  if(p!==ADMIN_PASS){alert("Wrong Password"); return;}
  document.getElementById("adminPage").classList.remove("hidden");
  document.getElementById("loginBox").classList.add("hidden");
  loadAdmin();
}

window.loadAdmin = function(){
  const usersRef = ref(db, 'users');
  onValue(usersRef, snapshot=>{
    const users = snapshot.val();
    adminData.innerHTML="";
    for(let key in users){
      const u = users[key];
      adminData.innerHTML += `
      <tr>
      <td>${u.name}</td>
      <td>${u.user}</td>
      <td>${u.mobile}</td>
      <td>${u.active?"Active":"Deactive"}</td>
      <td><button onclick="toggleUser('${key}',${u.active})">Toggle</button></td>
      </tr>`;
    }
  });
}

window.toggleUser = function(key, current){
  const userRef = ref(db, 'users/' + key);
  update(userRef, {active: !current});
}

window.filterUsers = function(){
  let filter=document.getElementById("searchUser").value.toLowerCase();
  let trs=adminData.getElementsByTagName("tr");
  for(let tr of trs){tr.style.display=tr.cells[1].innerText.toLowerCase().includes(filter)?"":"none";}
}

window.exportCSV = function(){
  const usersRef = ref(db, 'users');
  onValue(usersRef, snapshot=>{
    const users = snapshot.val();
    let csv="Name,Username,Mobile,Email,Status\n";
    for(let key in users){
      let u = users[key];
      csv+=`${u.name},${u.user},${u.mobile},${u.email},${u.active?"Active":"Deactive"}\n`;
    }
    let blob = new Blob([csv],{type:"text/csv"});
    let a=document.createElement("a");
    a.href=URL.createObjectURL(blob);
    a.download="users.csv";
    a.click();
  }, {onlyOnce:true});
}
</script>

</body>
</html>
