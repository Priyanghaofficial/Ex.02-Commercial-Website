# Ex02 Commercial Website
## Date:05.09.2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=1200, initial-scale=1.0" />
  <title>Curlora - Curly Hair Care</title>
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Belleza&family=Josefin+Sans:wght@400;700&family=Inder&family=Instrument+Sans:wght@400;600&display=swap" rel="stylesheet" />
  <script src="https://code.iconify.design/2/2.2.1/iconify.min.js"></script>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #FFFCFC;
      color: #201D1D;
      font-family: 'Josefin Sans', sans-serif;
      box-sizing: border-box;
    }

    /* HEADER */
    header {
      background: #FBEEA1;
      padding: 15px 0;
      position: relative;
      z-index: 2;
    }
    .navbar {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      height: 70px;
      width: 100vw;
      padding: 0 40px;
      box-sizing: border-box;
    }
    .navbar ul {
      display: flex;
      gap: 20px;
      list-style: none;
      margin: 0;
      padding: 0;
    }
    .navbar a {
      text-decoration: none;
      color: #1E1E1E;
      font-size: 18px;
    }
    .logo {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      font-family: 'Josefin Sans', sans-serif;
      font-weight: 700;
      font-size: 40px;
      color: #201D1D;
      width: 253px;
      height: 44px;
      text-align: center;
      line-height: 44px;
      z-index: 1;
    }
    .nav-left,
    .nav-icons {
      flex: 1;
      display: flex;
      align-items: center;
    }
    .nav-left {
      justify-content: flex-start;
    }
    .nav-icons {
      justify-content: flex-end;
      gap: 30px;
    }
    .nav-icons span {
      font-size: 20px;
      cursor: pointer;
      margin-left: 0;
    }

    /* HERO SECTION */
    .hero-container {
      display: flex;
      width: 100vw;
      min-height: 100vh;
      background: #fff;
    }
    .hero-text {
      width: 50vw;
      min-width: 350px;
      padding: 70px 35px 0 70px;
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: center;
    }
    .labels-row {
      margin-bottom: 18px;
      display: flex;
      gap: 16px;
    }
    .pill-label {
      border-radius: 16px;
      color: #fff;
      font-family: 'Inder', sans-serif;
      font-size: 22px;
      padding: 10px 25px;
      background: #E69BB8;
      width: fit-content;
      margin-right: 10px;
    }
    .pill-label.sub {
      background: #7BBEDD;
    }

    .hero-headline {
      font-family: 'Belleza', sans-serif;
      font-size: 95px;
      font-weight: 400;
      color: #201D1D;
      margin: 0 0 24px 0;
      line-height: 1.08;
      letter-spacing: 2px;
    }
    .btn-shop {
      background: #E4ABAB;
      color: #fff;
      border: none;
      border-radius: 14px;
      font-family: 'Inder', sans-serif;
      font-size: 23px;
      width: 186px;
      height: 54px;
      margin: 10px 0 40px;
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(228, 171, 171, 0.09);
      transition: background 0.2s;
    }
    .btn-shop:hover {
      background: #d89aa4;
    }
    .info-banner {
      margin-top: 50px;
      background: #F5EDAE;
      border-radius: 16px;
      width: 92%;
      min-height: 130px;
      padding: 32px 30px 30px 36px;
      font-family: 'Instrument Sans', 'Josefin Sans', sans-serif;
      font-size: 30px;
      font-weight: 400;
      line-height: 1.30;
      max-width: 600px;
      text-align: left;
      box-sizing: border-box;
    }
    .info-banner em {
      font-style: italic;
      font-weight: 600;
      color: #201D1D;
    }

    .hero-image-section {
      width: 46vw;
      display: flex;
      justify-content: flex-end;
      padding-top: 60px;
    }
    .model-img {
      width: 100%;
      height: 660px;
      object-fit: cover;
      border-radius: 18px;
      box-shadow: 0 10px 24px rgba(0,0,0,0.04);
    }

    /* RESPONSIVE */
    @media (max-width: 1200px) {
      .hero-headline { font-size: 7vw; }
      .info-banner { font-size: 2vw; }
      .model-img { height: 340px; }
    }
    @media (max-width: 900px) {
      .hero-container { flex-direction: column; }
      .hero-text, .hero-image-section { width: 100vw; }
      .model-img { height: 100px; width: 95vw; margin-top: 20px; }
      .hero-text { padding: 32px 5vw 0; }
      .info-banner { font-size: 16px; }
      .hero-headline { font-size: 36px; }
      .btn-shop { font-size: 17px; height: 44px; width: 130px; }
      .pill-label { font-size: 11px; }
    }

    /* Bestsellers */
    .bestsellers {
      text-align: center;
      padding: 60px 20px;
    }
    .bestsellers h2 {
      font-size: 42px;
      font-family: 'Belleza', sans-serif;
    }
    .bestsellers p {
      font-size: 24px;
      margin-bottom: 28px;
    }
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
    }
    .product-card img {
      width: 85%;
      border-radius: 7.5px;
      margin: 0 auto;
    }
    .product-card h3 { font-size: 18px; margin: 10px 0 5px; }
    .product-card p { font-size: 16px; color: #333; }
    .product-shop-btn {
      background: #E4ABAB;
      color: #fff;
      border: none;
      border-radius: 12px;
      font-size: 16px;
      width: 120px;
      height: 40px;
      margin: 13px auto 0;
      display: block;
      cursor: pointer;
    }
    .product-shop-btn:hover { background: #d89090; }

    /* Footer */
    footer {
      background: #E9E5CE;
      padding: 40px 0;
    }
    .footer-container {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
    .footer-column h3 { font-size: 30px; margin-bottom: 15px; }
    .footer-column li {
      font-size: 18px;
      margin-bottom: 10px;
      color: #74736F;
      list-style: none;
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <nav class="navbar">
      <div class="nav-left">
        <ul>
          <li><a href="#">SHOP</a></li>
          <li><a href="#">ABOUT US</a></li>
          <li><a href="#">NEW LAUNCH</a></li>
          <li><a href="#">BLOGS</a></li>
        </ul>
      </div>
      <div class="logo">CURLORA</div>
      <div class="nav-icons">
        <span class="iconify" data-icon="ic:outline-search"></span>
        <span class="iconify" data-icon="ic:outline-shopping-cart"></span>
        <span class="iconify" data-icon="ic:outline-person"></span>
      </div>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero-container">
    <div class="hero-text">
      <div class="labels-row">
        <span class="pill-label">SULPHATE FREE</span>
        <span class="pill-label sub">PARABEN FREE</span>
      </div>
      <h1 class="hero-headline">FRIZZ TAKING<br>OVER?</h1>
      <button class="btn-shop">SHOP NOW</button>
      <div class="info-banner">
        100% clean, salon quality products<br />
        <em>intentionally formulated for real, glorious, Indian hair.</em>
      </div>
    </div>
    <div class="hero-image-section">
      <img src="images/hero.jpg" alt="Curly Hair Model" class="model-img" />
    </div>
  </section>

  <!-- Bestsellers -->
  <section class="bestsellers">
    <h2>Bestsellers</h2>
    <p>Curl Community Favourites</p>
    <div class="product-grid">
      <div class="product-card">
        <img src="images/conditioner.jpg" alt="Leave-in Conditioner" />
        <h3>Curlora Leave-in Conditioner</h3>
        <p>From Rs. 599</p>
        <button class="product-shop-btn">Shop Now</button>
      </div>
      <div class="product-card">
        <img src="images/oil.jpg" alt="Hydrating Oil" />
        <h3>Curlora Hydrating Oil</h3>
        <p>From Rs. 699</p>
        <button class="product-shop-btn">Shop Now</button>
      </div>
      <div class="product-card">
        <img src="images/perfume.jpg" alt="Hair and Body Perfume" />
        <h3>Curlora Hair and Body Perfume</h3>
        <p>From Rs. 399</p>
        <button class="product-shop-btn">Shop Now</button>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="footer-container">
      <div class="footer-column">
        <h3>Your Curls</h3>
        <ul>
          <li>Curl Profile</li>
          <li>Curlcare</li>
          <li>Subscribe & Save</li>
          <li>Curls Routines</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>Your Order</h3>
        <ul>
          <li>FAQs</li>
          <li>Shipping</li>
          <li>Returns</li>
          <li>Rewards</li>
        </ul>
      </div>
      <div class="footer-column">
        <h3>Curlora</h3>
        <ul>
          <li>About Us</li>
          <li>Contact Us</li>
          <li>Store & Salon Locator</li>
          <li>Reviews</li>
        </ul>
      </div>
    </div>
  </footer>
</body>
</html>

```


## OUTPUT
<img width="1920" height="1080" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/f50548e9-44a5-4767-be77-eaf0c5b63943" />

<img width="1920" height="1080" alt="Screenshot (59)" src="https://github.com/user-attachments/assets/7d747a12-7b5b-4f22-a1a6-b652782fe4e9" />

<img width="1920" height="1080" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/e26ef55b-2f9b-4a67-bc84-fdc777b8eb79" />
<img width="1920" height="1080" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/087b82de-a57d-424e-81fe-e2b8d59757f2" />

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
