<SINGARYA>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SB COMENY | Modern Dashboard</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box}
body{
  margin:0;
  font-family:'Poppins',sans-serif;
  min-height:100vh;
  background:
    radial-gradient(circle at 20% 20%, #ff4ecd55, transparent 40%),
    radial-gradient(circle at 80% 30%, #4facfe55, transparent 40%),
    linear-gradient(135deg,#0f2027,#203a43,#2c5364);
  color:#fff;
}

/* NAME BADGE */
.name-badge{
  position:fixed;
  top:15px;
  left:20px;
  font-size:2rem;
  font-weight:800;
  letter-spacing:2px;
  background:linear-gradient(135deg,#ff416c,#ff4b2b,#f9d423);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  text-shadow:0 8px 30px rgba(0,0,0,.6);
  z-index:1000;
}

/* HEADER */
header{
  text-align:center;
  padding:30px 10px;
  font-size:2.1rem;
  font-weight:600;
}

/* LAYOUT */
.container{
  display:flex;
  gap:30px;
  flex-wrap:wrap;
  justify-content:center;
  padding-bottom:50px;
}

/* GLASS CARD */
.glass{
  background:rgba(255,255,255,0.12);
  backdrop-filter:blur(16px);
  border-radius:20px;
  box-shadow:0 20px 40px rgba(0,0,0,.4);
}

/* SIDEBAR */
.sidebar{
  width:260px;
  padding:25px;
  text-align:center;
}
.sidebar img{
  width:110px;
  height:110px;
  border-radius:50%;
  border:4px solid #fff;
}
.sidebar h3{margin:15px 0 5px}
.sidebar p{margin:0;font-size:.9rem;opacity:.9}

/* BUTTON */
.btn{
  width:100%;
  padding:12px;
  margin-top:12px;
  border:none;
  border-radius:12px;
  font-weight:600;
  cursor:pointer;
  transition:.3s;
}
.btn:hover{transform:translateY(-3px)}
.whatsapp{background:#25D366;color:#fff}
.call{background:#0d6efd;color:#fff}
.admin{background:linear-gradient(135deg,#ff416c,#ff4b2b);color:#fff}

/* MAIN */
.main{
  width:520px;
  padding:30px;
}
.card{
  margin-bottom:25px;
}
.card h3{text-align:center;margin-bottom:20px}

/* INPUT */
input{
  width:100%;
  padding:12px;
  margin:10px 0;
  border-radius:12px;
  border:none;
  outline:none;
}

/* TABLE */
table{
  width:100%;
  border-collapse:collapse;
  font-size:.9rem;
}
th,td{
  padding:10px;
  text-align:center;
}
th{background:rgba(0,0,0,.3)}
td{background:rgba(255,255,255,.08)}

/* MODAL */
.modal-bg{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.7);
  display:none;
  align-items:center;
  justify-content:center;
}
.modal{
  width:360px;
  padding:25px;
}

/* UTIL */
.hidden{display:none}
</style>
</head>

<body>

<!-- NAME -->
<div class="name-badge">MOHD BILAL</div>

<header>SB COMENY • Secure Service Portal</header>

<div class="container">

<div class="sidebar glass">
<img src="https://raw.githubusercontent.com/bilal8766/SB-COMENY/main/bilal%20khan%20photos.jpeg">
<h3>MOHD BILAL</h3>
<p>Owner</p>
<p>📞 9813490892</p>
<button class="btn whatsapp" onclick="window.open('https://wa.me/919813490892')">WhatsApp</button>
<button class="btn call" onclick="location.href='tel:9813490892'">Call</button>
<button class="btn admin" onclick="openAdmin()">ADMIN</button>
</div>

<div class="main glass">

<div class="card" id="loginBox">
<h3>Login</h3>
<input id="loginUser" placeholder="Username">
<input id="loginPass" type="password" placeholder="Password">
<button class="btn admin" onclick="login()">Login</button>
<p style="text-align:center;cursor:pointer" onclick="openModal()">Create Account</p>
</div>

<div class="card hidden" id="userPage">
<h3>User Profile</h3>
<div id="userInfo"></div>
<button class="btn admin" onclick="logout()">Logout</button>
</div>

<div class="card hidden" id="adminPage">
<h3>Admin Dashboard</h3>
<table>
<thead>
<tr><th>Name</th><th>User</th><th>Mobile</th><th>Status</th><th>Action</th></tr>
</thead>
<tbody id="adminData"></tbody>
</table>
</div>

</div>
</div>

<div class="modal-bg" id="regModal">
<div class="modal glass">
<h3>Create Account</h3>
<input id="rName" placeholder="Full Name">
<input id="rMobile" placeholder="Mobile">
<input id="rEmail" placeholder="Email">
<input id="rUser" placeholder="Username">
<input id="rPass" type="password" placeholder="Password">
<button class="btn admin" onclick="register()">Register</button>
<button class="btn" onclick="closeModal()">Cancel</button>
</div>
</div>

<script type="module">
import { initializeApp } from "https://www.gstatic.com/firebasejs/9.22.1/firebase-app.js";
import { getDatabase, ref, push, get, update } from "https://www.gstatic.com/firebasejs/9.22.1/firebase-database.js";

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

window.openModal=()=>regModal.style.display="flex";
window.closeModal=()=>regModal.style.display="none";

window.register=async()=>{
  const snap=await get(ref(db,"users"));
  const users=snap.val()||{};
  for(let k in users){ if(users[k].user===rUser.value) return alert("Username exists"); }
  await push(ref(db,"users"),{
    name:rName.value,mobile:rMobile.value,email:rEmail.value,
    user:rUser.value,pass:rPass.value,active:true
  });
  alert("Registered Successfully");
  closeModal();
};

window.login=async()=>{
  const snap=await get(ref(db,"users"));
  const users=snap.val()||{};
  for(let k in users){
    let u=users[k];
    if(u.user===loginUser.value && u.pass===loginPass.value){
      if(!u.active) return alert("Blocked");
      loginBox.classList.add("hidden");
      userPage.classList.remove("hidden");
      userInfo.innerHTML=`Name: ${u.name}<br>Mobile: ${u.mobile}<br>Email: ${u.email}`;
      return;
    }
  }
  alert("Wrong login");
};

window.openAdmin=async()=>{
  if(prompt("Admin Password")!==ADMIN_PASS) return alert("Wrong Password");
  adminPage.classList.remove("hidden");
  loginBox.classList.add("hidden");
  const snap=await get(ref(db,"users"));
  const users=snap.val()||{};
  adminData.innerHTML="";
  for(let k in users){
    let u=users[k];
    adminData.innerHTML+=`
      <tr>
        <td>${u.name}</td>
        <td>${u.user}</td>
        <td>${u.mobile}</td>
        <td>${u.active?"Active":"Off"}</td>
        <td><button onclick="toggleUser('${k}',${u.active})">Toggle</button></td>
      </tr>`;
  }
};

window.toggleUser=async(k,s)=>{
  await update(ref(db,"users/"+k),{active:!s});
  openAdmin();
};

window.logout=()=>location.reload();
</script>

</body>
</html>
