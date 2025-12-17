# -vyankatesh-jewellers
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vyankatesh Jewellers</title>

  <style>
    *{box-sizing:border-box;margin:0;padding:0;font-family:Segoe UI,Tahoma,Verdana,sans-serif}
    body{background:#fff;color:#333}
    header{background:#111;color:#fff;padding:20px 40px}
    header h1{font-size:28px;letter-spacing:2px}
    nav{margin-top:10px}
    nav a{color:#fff;margin-right:20px;text-decoration:none;font-size:14px}
    nav a:hover{text-decoration:underline}
    .hero{height:70vh;background:linear-gradient(rgba(0,0,0,.4),rgba(0,0,0,.4)),url('https://images.unsplash.com/photo-1606760227091-3dd870d97f1d') center/cover no-repeat;display:flex;align-items:center;justify-content:center;color:#fff;text-align:center}
    .hero h2{font-size:48px}
    section{padding:60px 40px}
    .section-title{text-align:center;font-size:32px;margin-bottom:40px}
    .about{max-width:900px;margin:auto;text-align:center;line-height:1.8}
    .contact{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:30px;max-width:900px;margin:auto}
    footer{background:#111;color:#fff;text-align:center;padding:20px;margin-top:40px}
  </style>
</head>

<body>

<!-- ================== SITE UNLOCKED: PUBLIC ACCESS ENABLED ================== -->
</div>

<header>
  <h1>Vyankatesh Jewellers</h1>
  <nav style="display:flex;align-items:center;justify-content:space-between">
  <div>
    <a href="#home">Home</a>
    <a href="#collections">Collections</a>
    <a href="#goldrate">Daily Gold Rate</a>
    <a href="#profile" id="profileLink" style="display:none">Profile</a>
    <a href="#contact">Contact</a>
  </div>
  <div style="display:flex;align-items:center;gap:20px">
    <div style="position:relative;cursor:pointer" onclick="openBasket()">
      <span style="font-size:22px">🛒</span>
      <span id="basketCount" style="position:absolute;top:-8px;right:-8px;background:red;color:white;border-radius:50%;padding:2px 6px;font-size:12px">0</span>
    </div>
    <a href="https://wa.me/918605523318" target="_blank" style="background:#25D366;color:white;padding:6px 12px;border-radius:20px;text-decoration:none;font-size:13px">WhatsApp</a>
  </div>
</nav>
</header>

<section class="hero" id="home">
  <div>
    <h2>Timeless Beauty</h2>
    <p>Exquisite jewellery crafted with elegance</p>
  </div>
</section>

<section id="collections">
  <h2 class="section-title">Gold Ring Collections</h2>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:25px;max-width:1000px;margin:auto">
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1600180758890-6b94519a8ba6" style="width:100%;border-radius:12px">
      <p>Classic Gold Ring</p>
    </div>
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f" style="width:100%;border-radius:12px">
      <p>Wedding Band Ring</p>
    </div>
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1606760227091-3dd870d97f1d" style="width:100%;border-radius:12px">
      <p>Designer Gold Ring</p>
    </div>
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1617038260897-41a1f14a8ca0" style="width:100%;border-radius:12px">
      <p>Traditional Ring</p>
    </div>
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1617038260897-41a1f14a8ca0" style="width:100%;border-radius:12px">
      <p>Daily Wear Gold Ring</p>
    </div>
    <div style="text-align:center">
      <img src="https://images.unsplash.com/photo-1584307833174-a0bb4b2c6f9b" style="width:100%;border-radius:12px">
      <p>Couple Ring Set</p>
    </div>
  </div>
  <p style="text-align:center;margin-top:30px">More exclusive gold ring designs available at our showroom.</p>
</section>

<section id="goldrate">
  <h2 class="section-title">Daily Gold Rate</h2>
  <div class="about">Please visit our shop for today's gold & silver rates.</div>
</section>

<section id="basket">
  <h2 class="section-title">Basket</h2>
  <div class="about">Selected jewellery items will appear here.</div>
</section>

<section id="profile" style="display:none">
  <h2 class="section-title">My Profile</h2>
  <div class="about">
    <p><strong>Email:</strong> <span id="profileEmail">Not logged in</span></p>
    <p><strong>Mobile:</strong> <span id="profileMobile">Not logged in</span></p>
    <br>
    <button onclick="logout()">Logout</button>
  </div>
</section>

<section id="contact">
  <h2 class="section-title">Contact Us</h2>
  <div class="contact">
    <div><strong>Address</strong><br>Vyankatesh Jewellers, Latur 413512</div>
    <div><strong>Phone</strong><br>+91 86055 23318</div>
    <div><strong>Email</strong><br>mahesh.pushkar121@gmail.com</div>
  </div>
</section>

<footer>
  © 2025 Vyankatesh Jewellers<br>
  <small>Trusted Jewellery Showroom • Latur</small>
</footer>

<!-- ================== BASKET MODAL ================== -->
<div id="basketModal" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.7);z-index:4000">
  <div style="background:#fff;max-width:400px;margin:10% auto;padding:25px;border-radius:10px;text-align:center">
    <h3>Your Basket</h3><br>
    <p>No items added yet.</p>
    <br><button onclick="closeBasket()">Close</button>
  </div>
</div>

<!-- ================== LOGIN MODAL ================== -->
<div id="loginModal" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.7);z-index:3000">
  <div style="background:#fff;max-width:400px;margin:10% auto;padding:25px;border-radius:10px;text-align:center">
    <h3>Login</h3><br>

    <div id="step1">
      <input id="userEmail" type="email" placeholder="Enter Email" style="width:100%;padding:10px"><br><br>
      <input id="userMobile" type="tel" placeholder="Enter Mobile" style="width:100%;padding:10px"><br><br>
      <button onclick="loginUser()">Login</button>
    </div>

    <br><button onclick="closeLogin()">Close</button>
  </div>
</div>

<!-- ================== SCRIPT ================== -->
<script>
  function openLogin(){
    document.getElementById('loginModal').style.display = 'block';
  }

  function closeLogin(){
    document.getElementById('loginModal').style.display = 'none';
  }

  function loginUser(){
    const email = document.getElementById('userEmail').value.trim();
    const mobile = document.getElementById('userMobile').value.trim();

    if(!email){
      alert('Please enter email');
      return;
    }

    localStorage.setItem('profileEmail', email);
    localStorage.setItem('profileMobile', mobile || '');
    closeLogin();
    loadProfile();
  }

  function loadProfile(){
    const email = localStorage.getItem('profileEmail');
    const mobile = localStorage.getItem('profileMobile');

    if(email){
      document.getElementById('profileEmail').innerText = email;
      document.getElementById('profileMobile').innerText = mobile || '-';
      document.getElementById('profile').style.display = 'block';
      document.getElementById('profileLink').style.display = 'inline';
    } else {
      document.getElementById('profile').style.display = 'none';
      document.getElementById('profileLink').style.display = 'none';
    }
  }

  function logout(){
    localStorage.removeItem('profileEmail');
    localStorage.removeItem('profileMobile');
    loadProfile();
  }

  function openBasket(){
    document.getElementById('basketModal').style.display='block';
  }

  function closeBasket(){
    document.getElementById('basketModal').style.display='none';
  }

  loadProfile();
</script>

</body>
</html>
