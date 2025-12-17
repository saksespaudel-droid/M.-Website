# M.-Website
my personal website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>M.</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
    margin: 0;
    font-family: 'Poppins', 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ffe0ec, #fff5f9);
    color: #333;
    overflow-x: hidden;
}

/* HEADER */
header {
    background: linear-gradient(135deg, #ff6fa5, #ff9acb);
    color: white;
    text-align: center;
    padding: 90px 20px;
    position: relative;
}

header h1 {
    font-size: 4rem;
    margin: 0;
    letter-spacing: 3px;
}

header p {
    margin-top: 12px;
    font-size: 1.2rem;
}

/* SECTION */
section {
    max-width: 900px;
    margin: auto;
    padding: 45px 20px;
}

.card {
    background: white;
    padding: 35px;
    border-radius: 22px;
    box-shadow: 0 18px 35px rgba(255, 111, 165, 0.25);
    margin-bottom: 35px;
}

/* PHOTO */
.photo-box img {
    width: 100%;
    border-radius: 18px;
}

/* COUNTDOWN */
#countdown {
    font-size: 1.4rem;
    color: #ff6fa5;
    font-weight: bold;
}

/* HEARTS */
.heart {
    position: fixed;
    bottom: -20px;
    color: rgba(255, 105, 180, 0.6);
    font-size: 20px;
    animation: floatUp 8s linear infinite;
}

@keyframes floatUp {
    0% {
        transform: translateY(0) scale(1);
        opacity: 0;
    }
    10% { opacity: 1; }
    100% {
        transform: translateY(-110vh) scale(1.6);
        opacity: 0;
    }
}

footer {
    background: #ff6fa5;
    color: white;
    text-align: center;
    padding: 18px;
    font-size: 0.95rem;
}
</style>
</head>

<body>

<header>
    <h1>M.</h1>
    <p>Some people stay special, even with time 💗</p>
</header>

<section>

<div class="card">
<h2>Her Birthday 🎂</h2>
<p><strong>Nepali Date:</strong> Magh 21</p>
<p><strong>English Date:</strong> February 24</p>
<p id="countdown"></p>
</div>

<div class="card">
<h2>Photo Memory 📷</h2>
<div class="photo-box">
    <!-- Replace "her-photo.jpg" with the real photo name -->
    <img src="her-photo.jpg" alt="M.">
</div>
<p style="color:#777; font-size:0.9rem; margin-top:10px;">
(You can change or remove the photo anytime)
</p>
</div>

<div class="card">
<h2>Unsent Words 💌</h2>
<p>
This page doesn’t ask for anything back.
It’s just a quiet wish for happiness,
especially on a day that still matters.
</p>
<p>
Happy Birthday, M. 💗
</p>
</div>

</section>

<footer>
<p>Made with respect, memories & silence 💗</p>
</footer>

<!-- COUNTDOWN SCRIPT -->
<script>
const birthday = new Date("February 24, 2026 00:00:00").getTime();

setInterval(() => {
    const now = new Date().getTime();
    const diff = birthday - now;

    if (diff > 0) {
        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
        const mins = Math.floor((diff / (1000 * 60)) % 60);

        document.getElementById("countdown").innerHTML =
            days + " days, " + hours + " hours, " + mins + " minutes left";
    } else {
        document.getElementById("countdown").innerHTML =
            "Today is her birthday 🎉";
    }
}, 1000);

/* FLOATING HEARTS */
function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (14 + Math.random() * 20) + "px";
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 8000);
}
setInterval(createHeart, 600);
</script>

</body>
</html>
