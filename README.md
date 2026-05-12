<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tech Reviews</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Orbitron:wght@500&family=Space+Mono&family=DM+Sans&display=swap" rel="stylesheet">

  <link rel="stylesheet" href="styles.css">
</head>
<body>

<!-- Cursor -->
<div class="cursor"></div>

<!-- NAV -->
<nav class="nav">
  <h1 class="logo">TECHLAB</h1>
  <ul>
    <li>Reviews</li>
    <li>Compare</li>
    <li>Brands</li>
  </ul>
  <button class="cta">Subscribe</button>
</nav>

<!-- NEWS TICKER -->
<div class="ticker">
  <div class="ticker-text">LATEST: iPhone 15 Review • Galaxy S24 Ultra • Pixel 9 Leak •</div>
</div>

<!-- HERO -->
<section class="hero">
  <div class="hero-text">
    <h1>Future Tech Reviews</h1>
    <p>Brutally honest. Data-driven. No fluff.</p>
  </div>
  <div class="hero-card">🔥 Featured Review</div>
</section>

<!-- FILTER -->
<section class="filter">
  <button onclick="filterBrand('all')">All</button>
  <button onclick="filterBrand('apple')">Apple</button>
  <button onclick="filterBrand('samsung')">Samsung</button>
</section>

<!-- PRODUCT GRID -->
<section class="grid">
  <div class="card apple">
    <h2>iPhone 15</h2>
    <p>Score: 9.2</p>
  </div>

  <div class="card samsung">
    <h2>Galaxy S24</h2>
    <p>Score: 9.0</p>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 TECHLAB</p>
</footer>

<script src="script.js"></script>
</body>
</html>body {
  margin: 0;
  background: #0a0a0a;
  color: white;
  font-family: 'DM Sans', sans-serif;
}

/* Grain overlay */
body::after {
  content: "";
  position: fixed;
  inset: 0;
  background: url('https://grainy-gradients.vercel.app/noise.svg');
  opacity: 0.05;
  pointer-events: none;
}

/* NAV */
.nav {
  position: fixed;
  width: 100%;
  display: flex;
  justify-content: space-between;
  backdrop-filter: blur(10px);
  padding: 15px 30px;
}

/* Ticker */
.ticker {
  margin-top: 70px;
  overflow: hidden;
  background: #e8ff35;
  color: black;
}
.ticker-text {
  white-space: nowrap;
  animation: scroll 10s linear infinite;
}
@keyframes scroll {
  from { transform: translateX(100%); }
  to { transform: translateX(-100%); }
}

/* HERO */
.hero {
  display: flex;
  justify-content: space-between;
  padding: 100px 50px;
}

.hero h1 {
  font-family: 'Bebas Neue';
  font-size: 64px;
}

/* CARD */
.card {
  background: #111;
  padding: 20px;
  margin: 20px;
  transition: transform 0.3s;
  perspective: 1000px;
}

.card:hover {
  transform: rotateY(10deg) rotateX(10deg);
}

/* BUTTON */
button {
  background: #e8ff35;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
}// Brand Filter
function filterBrand(brand) {
  let cards = document.querySelectorAll('.card');

  cards.forEach(card => {
    if (brand === 'all' || card.classList.contains(brand)) {
      card.style.display = 'block';
    } else {
      card.style.display = 'none';
    }
  });
}

// Custom Cursor
const cursor = document.querySelector('.cursor');

document.addEventListener('mousemove', e => {
  cursor.style.left = e.clientX + 'px';
  cursor.style.top = e.clientY + 'px';
});
