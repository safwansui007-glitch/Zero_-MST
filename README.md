<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ZERO MST – Official Site</title>

<meta name="description" content="ZERO MST – Eco friendly flavour device. No smoke. No chemicals. Pure flavour.">
<meta name="theme-color" content="#00ffe5">

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap');

body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: #0a0a0d;
    color: #eee;
    transition: 0.5s ease-in-out;
}

/* ---------------- LOADER -------------- */
#loader {
    position: fixed;
    inset: 0;
    background: #000;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    z-index: 99999;
}
.ring {
    width: 80px;
    height: 80px;
    border: 6px solid #00ffe5;
    border-top: 6px solid transparent;
    border-radius: 50%;
    animation: spin 1s linear infinite;
}
@keyframes spin { to { transform: rotate(360deg); } }
#loader p {
    color: #00ffe5;
    margin-top: 10px;
    font-size: 22px;
}

/* ---------------- THEME BUTTONS -------------- */
#themeBtn, #neonBtn {
    position: fixed;
    right: 20px;
    padding: 10px 18px;
    border-radius: 10px;
    font-weight: 700;
    cursor: pointer;
    border: none;
    z-index: 9999;
}
#themeBtn {
    top: 20px;
    background: #00ffe5;
    color: #000;
}
#neonBtn {
    top: 70px;
    background: #0077ff;
    color: white;
}

/* ---------------- INTRO -------------- */
.intro {
    text-align: center;
    padding: 120px 20px;
}
.intro h1 {
    font-size: 70px;
    color: #00ffe5;
    animation: glow 2s infinite alternate;
}
@keyframes glow {
    0% { text-shadow: 0 0 15px #00ffe5; }
    100% { text-shadow: 0 0 40px #00ffe5; }
}
.intro p {
    color: #9af7f2;
    font-size: 24px;
}

/* ---------------- LOGO -------------- */
.logo-glow {
    text-align: center;
    font-size: 60px;
    font-weight: 900;
    color: #00ffe5;
    letter-spacing: 4px;
    animation: glow2 2s infinite alternate;
}
@keyframes glow2 {
    0% { text-shadow: 0 0 12px #00ffe5; }
    100% { text-shadow: 0 0 35px #00ffe5; }
}

/* ---------------- SECTIONS -------------- */
.section {
    padding: 60px 25px;
    text-align: center;
}
.section h2 {
    font-size: 38px;
    color: #00ffe5;
    text-transform: uppercase;
}

/* ---------------- MODELS -------------- */
.models {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 35px;
}
.card {
    width: 330px;
    padding: 30px;
    background: #141418;
    border-radius: 20px;
    border: 1px solid #00ffe5;
    transition: 0.3s;
}
.card:hover {
    transform: scale(1.07);
    box-shadow: 0 0 30px rgba(0,255,200,0.8);
}
.price {
    font-size: 28px;
    color: #5dfff3;
    font-weight: 700;
}
.special {
    margin-top: 10px;
    padding: 8px;
    background: #ffe49b;
    border-radius: 10px;
    font-weight: bold;
}

/* ---------------- FLAVOURS -------------- */
.flavours {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}
.flav {
    padding: 15px 20px;
    background: #111;
    border-radius: 12px;
    border: 1px solid #0098ff;
    font-size: 18px;
    display: flex;
    align-items: center;
    gap: 10px;
}
.fimg {
    width: 40px;
    height: 40px;
    border-radius: 8px;
    object-fit: cover;
    transition: 0.3s;
}
.fimg:hover {
    transform: scale(1.2) rotate(10deg);
}

/* ---------------- ORDER FORM -------------- */
.order-box {
    width: 360px;
    margin: auto;
    padding: 25px;
    background: #111;
    border-radius: 15px;
    border: 1px solid #00ffe5;
}
.order-box input,
.order-box select,
.order-box textarea {
    width: 100%;
    margin-top: 10px;
    padding: 12px;
    border-radius: 8px;
    border: none;
    outline: none;
    background: #222;
    color: #fff;
}
.order-box button {
    width: 100%;
    padding: 12px;
    margin-top: 15px;
    background: #00ffe5;
    color: #000;
    border: none;
    border-radius: 10px;
    font-weight: bold;
    cursor: pointer;
}

/* ---------------- POPUP -------------- */
#thankPopup {
    position: fixed;
    inset: 0;
    display: none;
    justify-content: center;
    align-items: center;
    background: rgba(0,0,0,0.8);
    z-index: 9999;
}
.popup-box {
    background: #00ffe5;
    padding: 30px;
    border-radius: 15px;
    text-align: center;
    color: #000;
    font-weight: bold;
}

/* ---------------- FOOTER -------------- */
footer {
    background: #0077ff;
    padding: 20px;
    text-align: center;
    color: #000;
    font-weight: bold;
}

/* ---------------- FULL LIGHT MODE FIX -------------- */
.light-mode {
    background: #f8ffff !important;
    color: #000 !important;
}
.light-mode .intro h1,
.light-mode .logo-glow,
.light-mode h2 {
    color: #007d7d !important;
    text-shadow: none !important;
}
.light-mode .card {
    background: #ffffff !important;
    border: 1px solid #00bfa5 !important;
    box-shadow: none !important;
}
.light-mode .flav {
    background: #e8faff !important;
    border-color: #00aaff !important;
    color: #003a5a !important;
}
.light-mode .order-box {
    background: #ffffff !important;
    border-color: #00bfa5 !important;
}
.light-mode input,
.light-mode select,
.light-mode textarea {
    background: #f4f4f4 !important;
    color: #000 !important;
    border: 1px solid #00bfa5 !important;
}
.light-mode footer {
    background: #00a0a0 !important;
    color: #fff !important;
}
.light-mode #themeBtn {
    background: #009999 !important;
    color: #fff !important;
}

/* ---------------- NEON MODE ---------------- */
.dark-neon {
    background: #000015 !important;
    color: #00f7ff !important;
}
.dark-neon .card,
.dark-neon .order-box {
    background: #010126 !important;
    border-color: #00eaff !important;
    box-shadow: 0 0 25px #00eaff !important;
}
.dark-neon .flav {
    background: #02022d !important;
    border-color: #00c8ff !important;
    color: #cfffff !important;
}
.dark-neon footer {
    background: #001a33;
    color: #00eaff !important;
}
.dark-neon #neonBtn {
    background: #00eaff !important;
    color: #000 !important;
}
.dark-neon #themeBtn {
    background: #00ffe5 !important;
    color: #000 !important;
}

</style>
</head>

<body>

<!-- Buttons -->
<button id="themeBtn" onclick="document.body.classList.toggle('light-mode')">Light Mode</button>
<button id="neonBtn" onclick="document.body.classList.toggle('dark-neon')">Neon Mode</button>

<!-- Loader -->
<div id="loader">
    <div class="ring"></div>
    <p>ZERO MST</p>
</div>

<script>
window.onload = () => {
    setTimeout(() => {
        document.getElementById("loader").style.display = "none";
    }, 400);
};
</script>

<!-- Intro -->
<div class="intro">
    <h1>ZERO MST</h1>
    <p>Pure Flavour • Zero Chemicals • Zero Smoke</p>
</div>

<!-- Logo -->
<div class="logo-glow">ZERO MST</div>

<!-- Models -->
<section class="section">
    <h2>Models</h2>
    <div class="models">
        <div class="card">
            <h3>Model 1 — Small</h3>
            <p>Simple & smooth.</p>
            <div class="price">0.75 AED</div>
        </div>

        <div class="card">
            <h3>Model 2 — Normal</h3>
            <p>Perfect daily model.</p>
            <div class="price">1 AED</div>
        </div>

        <div class="card">
            <h3>Model 3 — Premium</h3>
            <p>High performance.</p>
            <div class="price">2 / 3 / 4 AED</div>
            <div class="special">🔥 4 AED = ULTRA BANGER MODE</div>
        </div>
    </div>
</section>

<!-- Flavours -->
<section class="section">
    <h2>Flavours</h2>
    <div class="flavours">
        <div class="flav"><img src="mint.png" class="fimg"> Mint Ice</div>
        <div class="flav"><img src="blueberry.png" class="fimg"> Blueberry Rush</div>
        <div class="flav"><img src="watermelon.png" class="fimg"> Watermelon Frost</div>
        <div class="flav"><img src="peach.png" class="fimg"> Peach Breeze</div>
        <div class="flav"><img src="grape.png" class="fimg"> Grape Storm</div>
        <div class="flav"><img src="lemon.png" class="fimg"> Lemon Spark</div>
    </div>
</section>

<!-- Order Form -->
<section class="section">
    <h2>Order Now</h2>
    <form class="order-box" action="https://formspree.io/f/meowvryg" method="POST" onsubmit="showThanksPopup()">
        
        <label>Your Name</label>
        <input type="text" name="name" required>

        <label>Your Email</label>
        <input type="email" name="email" required>

        <label>Phone (optional)</label>
        <input type="text" name="phone">

        <label>Select Model</label>
        <select name="model" required>
            <option>Model 1 (0.75 AED)</option>
            <option>Model 2 (1 AED)</option>
            <option>Model 3 (2/3/4 AED)</option>
        </select>

        <label>Quantity</label>
        <input type="number" name="quantity" min="1" value="1">

        <label>Message (optional)</label>
        <textarea name="message" rows="3"></textarea>

        <button type="submit">Submit Order</button>
    </form>
</section>

<!-- Popup -->
<div id="thankPopup">
    <div class="popup-box">
        <h3>Order Submitted 🎉</h3>
        <p>We received your order!</p>
    </div>
</div>

<script>
function showThanksPopup() {
    document.getElementById("thankPopup").style.display = "flex";
    setTimeout(() => {
        window.location.href = "thankyou.html";
    }, 2000);
}
</script>

<!-- Footer -->
<footer>
    © 2025 ZERO MST – No Smoke. Pure Flavour.
</footer>

</body>
</html>
