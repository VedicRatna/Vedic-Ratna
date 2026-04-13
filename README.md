<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Vedic Ratna Cosmetics</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    *{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
    body{background:#ffffff;color:#0f2e1c}

    header{display:flex;justify-content:space-between;align-items:center;padding:15px 50px;background:#0f2e1c}
    header .logo{display:flex;align-items:center;gap:10px}
    header img{height:40px}
    header h1{color:#ffffff;font-size:22px}
    nav a{margin:0 15px;text-decoration:none;color:#ffffff}

    .hero{height:90vh;display:flex;align-items:center;justify-content:center;flex-direction:column;text-align:center;background:linear-gradient(to right,#0f2e1c,#1f5c3a);color:#fff}
    .hero h2{font-size:48px}
    .hero p{margin:10px 0}

    .btn{padding:12px 25px;background:#1f5c3a;color:#fff;border:none;border-radius:25px;cursor:pointer;transition:0.3s}
    .btn:hover{background:#14422a}

    .products{padding:60px 50px;text-align:center}
    .product-grid{display:flex;gap:20px;justify-content:center;flex-wrap:wrap}
    .card{width:260px;padding:20px;border-radius:15px;background:#fff;box-shadow:0 5px 15px rgba(0,0,0,0.1);opacity:0;transform:translateY(40px);transition:0.6s}
    .card.show{opacity:1;transform:translateY(0)}
    .card img{width:100%;border-radius:10px}

    .gallery{padding:60px 50px;text-align:center;background:#f5f5f5}
    .gallery-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:15px}
    .gallery img{width:100%;border-radius:10px;opacity:0;transform:scale(0.9);transition:0.6s}
    .gallery img.show{opacity:1;transform:scale(1)}

    .contact{padding:60px 50px;text-align:center}
    form{max-width:400px;margin:auto;display:flex;flex-direction:column;gap:10px}
    input,textarea{padding:10px;border-radius:8px;border:1px solid #ccc}

    footer{text-align:center;padding:20px;background:#0f2e1c;color:#fff}
  </style>
</head>
<body>

<header>
  <div class="logo">
    <img src="https://via.placeholder.com/100x40?text=Logo" alt="Logo">
    <h1>Vedic Ratna</h1>
  </div>
  <nav>
    <a href="#">Home</a>
    <a href="#products">Products</a>
    <a href="#gallery">Gallery</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero">
  <h2>Elevate Your Skin Care Routine</h2>
  <p>Premium cosmetic solutions crafted for modern beauty</p>
  <button class="btn">Shop Now</button>
</section>

<section class="products" id="products">
  <h2>Our Products</h2>
  <div class="product-grid">

    <div class="card">
      <img src="https://via.placeholder.com/260" alt="Face Wash">
      <h3>Face Wash</h3>
      <p>Gentle daily cleansing</p>
      <button class="btn" onclick="alert('Contact us to order')">Buy Now</button>
    </div>

    <div class="card">
      <img src="https://via.placeholder.com/260" alt="Detan Pack">
      <h3>Detan Pack</h3>
      <p>Removes tan & brightens</p>
      <button class="btn" onclick="alert('Contact us to order')">Buy Now</button>
    </div>

    <div class="card">
      <img src="https://via.placeholder.com/260" alt="Serum">
      <h3>Vitamin C Serum</h3>
      <p>Radiance & nourishment</p>
      <button class="btn" onclick="alert('Contact us to order')">Buy Now</button>
    </div>

  </div>
</section>

<section class="gallery" id="gallery">
  <h2>Our Gallery</h2>
  <div class="gallery-grid">
    <img src="https://via.placeholder.com/300">
    <img src="https://via.placeholder.com/300">
    <img src="https://via.placeholder.com/300">
    <img src="https://via.placeholder.com/300">
  </div>
</section>

<section class="contact" id="contact">
  <h2>Contact Us</h2>
  <form onsubmit="sendMessage(event)">
    <input type="text" placeholder="Your Name" required>
    <input type="email" placeholder="Your Email" required>
    <textarea placeholder="Your Message" required></textarea>
    <button class="btn">Send Message</button>
  </form>
</section>

<footer>
  <p>© 2026 Vedic Ratna Cosmetics</p>
</footer>

<script>
function sendMessage(e){
  e.preventDefault();
  alert('Message sent! We will contact you soon.');
}

// Scroll animation
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add('show');
    }
  });
});

document.querySelectorAll('.card, .gallery img').forEach(el => observer.observe(el));
</script>

</body>
</html>
