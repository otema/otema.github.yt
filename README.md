<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TECHLAB</title>

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Orbitron:wght@500&family=Space+Mono&family=DM+Sans&display=swap" rel="stylesheet">

  <link rel="stylesheet" href="styles.css">
</head>
<body>

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

<!-- TICKER -->
<div class="ticker">
  <div class="ticker-text">LATEST: iPhone 15 • Galaxy S24 • Pixel 9 • OnePlus 12 •</div>
</div>

<!-- HERO -->
<section class="hero reveal">
  <div>
    <h1>Future Tech Reviews</h1>
    <p>Brutally honest. Data-driven. No fluff.</p>
  </div>
</section>

<!-- FILTER -->
<section class="filter reveal">
  <button onclick="filterBrand('all')">All</button>
  <button onclick="filterBrand('apple')">Apple</button>
  <button onclick="filterBrand('samsung')">Samsung</button>
</section>

<!-- GRID -->
<section class="grid">

  <div class="card apple reveal">
    <h2>iPhone 15</h2>
    <p>Score: 9.2</p>
  </div>

  <div class="card samsung reveal">
    <h2>Galaxy S24</h2>
    <p>Score: 9.0</p>
  </div>

  <div class="card apple reveal">
    <h2>MacBook Pro M3</h2>
    <p>Score: 9.5</p>
  </div>

</section>

<footer>
  <p>© 2026 TECHLAB</p>
</footer>

<script src="script.js"></script>
</body>
</html>
