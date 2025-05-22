<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Digital Agency - Creative Solutions</title>
<style>
  /* Reset and base */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    background: #f9fafc;
    color: #333;
  }
  a {
    text-decoration: none;
    color: inherit;
  }
  img {
    max-width: 100%;
    height: auto;
    display: block;
  }

  /* Container */
  .container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
  }

  /* Header */
  header {
    background: #00214d;
    color: #ffffff;
    padding: 1.2rem 0;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  header h1 {
    font-size: 1.8rem;
    font-weight: 700;
    letter-spacing: 1.5px;
  }
  nav ul {
    list-style: none;
    display: flex;
    gap: 2rem;
  }
  nav ul li a {
    color: #ffffffcc;
    font-weight: 600;
    transition: color 0.3s ease;
  }
  nav ul li a:hover {
    color: #00baff;
  }

  /* Hero Section */
  .hero {
    background: linear-gradient(135deg, #00baff 0%, #007aad 100%);
    color: #fff;
    padding: 6rem 0 4rem;
    text-align: center;
  }
  .hero h2 {
    font-size: 3rem;
    margin-bottom: 1rem;
    font-weight: 800;
    text-shadow: 1px 1px 4px rgba(0,0,0,0.4);
  }
  .hero p {
    font-size: 1.25rem;
    max-width: 600px;
    margin: 0 auto 2.5rem;
    text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
  }
  .btn-primary {
    background-color: #ffd500;
    color: #003a6f;
    font-weight: 700;
    padding: 0.75rem 2rem;
    border-radius: 50px;
    box-shadow: 0 5px 15px rgba(255, 213, 0, 0.4);
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    border: none;
    font-size: 1.1rem;
  }
  .btn-primary:hover {
    background-color: #e6c500;
    box-shadow: 0 8px 20px rgba(230, 197, 0, 0.6);
  }

  /* Services */
  .services {
    padding: 5rem 0 3rem;
    background: #ffffff;
  }
  .services h3 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 2rem;
    color: #00214d;
    font-weight: 700;
  }
  .service-list {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    gap: 2rem;
  }
  .service-card {
    background: #f0f6ff;
    padding: 2rem 1.5rem;
    border-radius: 12px;
    box-shadow: 0 8px 16px rgba(0,33,77,0.1);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .service-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 30px rgba(0,33,77,0.2);
  }
  .service-card svg {
    fill: #007aad;
    width: 48px;
    height: 48px;
    margin-bottom: 1rem;
  }
  .service-card h4 {
    margin-bottom: 1rem;
    font-size: 1.25rem;
    color: #003a6f;
  }
  .service-card p {
    font-size: 1rem;
    color: #425466;
  }

  /* Portfolio */
  .portfolio {
    background: #f9fafc;
    padding: 5rem 0 3rem;
  }
  .portfolio h3 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 2rem;
    color: #00214d;
    font-weight: 700;
  }
  .portfolio-grid {
    display: grid;
    gap: 1.5rem;
    grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
  }
  .portfolio-item {
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 8px 20px rgba(0,33,77,0.1);
    background: white;
    cursor: pointer;
    transition: transform 0.3s ease;
  }
  .portfolio-item:hover {
    transform: scale(1.05);
    box-shadow: 0 12px 30px rgba(0,33,77,0.2);
  }
  .portfolio-item img {
    display: block;
    width: 100%;
    height: 180px;
    object-fit: cover;
  }
  .portfolio-item .portfolio-info {
    padding: 1rem 1.2rem;
  }
  .portfolio-item .portfolio-info h4 {
    color: #003a6f;
    font-weight: 700;
    margin-bottom: 0.4rem;
  }
  .portfolio-item .portfolio-info p {
    color: #617488;
    font-size: 0.9rem;
  }

  /* About Us */
  .about {
    padding: 5rem 0 3rem;
    background: #00214d;
    color: #ffffffee;
  }
  .about .container {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 2rem;
  }
  .about .about-text {
    flex: 1 1 400px;
  }
  .about .about-text h3 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    font-weight: 700;
  }
  .about .about-text p {
    font-size: 1.1rem;
    line-height: 1.7;
  }
  .about .about-img {
    flex: 1 1 350px;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(255,255,255,0.07);
  }
  .about .about-img img {
    display: block;
    width: 100%;
    height: auto;
  }

  /* Contact */
  .contact {
    padding: 5rem 0 5rem;
    background: #f0f6ff;
  }
  .contact h3 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 2rem;
    color: #00214d;
    font-weight: 700;
  }
  .contact form {
    max-width: 600px;
    margin: 0 auto;
    background: white;
    padding: 2rem 2.5rem;
    border-radius: 12px;
    box-shadow: 0 8px 20px rgba(0,33,77,0.1);
  }
  .contact form .form-control {
    margin-bottom: 1.5rem;
  }
  .contact form label {
    display: block;
    font-weight: 600;
    margin-bottom: 0.5rem;
    color: #004080;
  }
  .contact form input,
  .contact form textarea {
    width: 100%;
    padding: 0.75rem 1rem;
    font-size: 1rem;
    border: 2px solid #c5d0de;
    border-radius: 10px;
    transition: border-color 0.3s ease;
  }
  .contact form input:focus,
  .contact form textarea:focus {
    outline: none;
    border-color: #007aad;
    box-shadow: 0 0 8px #007aad66;
  }
  .contact form textarea {
    resize: vertical;
    min-height: 120px;
  }
  .contact form button {
    background-color: #007aad;
    color: white;
    border: none;
    padding: 0.9rem 2rem;
    border-radius: 50px;
    font-weight: 700;
    font-size: 1.1rem;
    cursor: pointer;
    transition: background-color 0.3s ease;
    box-shadow: 0 5px 15px rgba(0, 122, 173, 0.4);
  }
  .contact form button:hover {
    background-color: #005887;
    box-shadow: 0 8px 20px rgba(0, 88, 135, 0.6);
  }

  /* Footer */
  footer {
    background: #001b3a;
    color: #7a8bb4;
    text-align: center;
    padding: 1.5rem 1rem;
    font-size: 0.9rem;
    font-weight: 400;
    letter-spacing: 1px;
  }

  /* Responsive */
  @media (max-width: 700px) {
    header .container {
      flex-direction: column;
      gap: 1rem;
    }
    .about .container {
      flex-direction: column;
    }
    .hero h2 {
      font-size: 2.25rem;
    }
  }
</style>
</head>
<body>
<header>
  <div class="container">
    <h1>BrightWave Agency</h1>
    <nav>
      <ul>
        <li><a href="#services">Services</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<section class="hero" id="home">
  <div class="container">
    <h2>Crafting Digital Experiences<br />That Inspire & Drive Growth</h2>
    <p>Your partner in creative web design, branding, and digital marketing solutions tailored to your business.</p>
    <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'});">Get in Touch</button>
  </div>
</section>

<section class="services container" id="services">
  <h3>Our Services</h3>
  <div class="service-list">
    <div class="service-card">
      <svg viewBox="0 0 64 64" aria-hidden="true" focusable="false"><path d="M32 4a28 28 0 1 0 28 28A28.032 28.032 0 0 0 32 4Zm0 52a24 24 0 1 1 24-24 24.027 24.027 0 0 1-24 24Z"/><path d="M37.25 16.69v14.06l11.22 6.81-3.87 6.75-11.21-6.8v14.06H27.5V37.47l-11.2 6.8-3.87-6.75 11.2-6.81v-14Zm-7.88 12.7 5.94 3.6v-7.19Z"/></svg>
      <h4>Web Design</h4>
      <p>Modern, responsive websites that engage your audience and convert visitors into customers.</p>
    </div>
    <div class="service-card">
      <svg viewBox="0 0 64 64" aria-hidden="true" focusable="false"><path d="M16 52v-6h32v6zm0-18v-6h32v6zm0-18v-6h32v6z"/></svg>
      <h4>Branding</h4>
      <p>Build a powerful brand identity with logos, messaging, and visuals that stand out.</p>
    </div>
    <div class="service-card">
      <svg viewBox="0 0 64 64" aria-hidden="true" focusable="false"><path d="M56 24H36v-4a4 4 0 0 0-8 0v4H8l24 20zM28 44a8 8 0 0 0 16 0v-8H28Z"/></svg>
      <h4>Digital Marketing</h4>
      <p>Targeted marketing strategies including SEO, PPC, and social media management.</p>
    </div>
  </div>
</section>

<section class="portfolio container" id="portfolio">
  <h3>Our Portfolio</h3>
  <div class="portfolio-grid">
    <div class="portfolio-item" tabindex="0" aria-label="Project Redesign for FinTech Co.">
      <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=600&q=80" alt="FinTech website redesign" />
      <div class="portfolio-info">
        <h4>FinTech Co. Website</h4>
        <p>Revamped UX/UI for improved customer engagement and conversions.</p>
      </div>
    </div>
    <div class="portfolio-item" tabindex="0" aria-label="Branding for Organic Foods Store">
      <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=600&q=80" alt="Organic food store branding materials" />
      <div class="portfolio-info">
        <h4>Organic Foods Branding</h4>
        <p>Created a fresh brand identity and packaging design that connects with eco-conscious customers.</p>
      </div>
    </div>
    <div class="portfolio-item" tabindex="0" aria-label="Social media marketing campaign for travel agency">
      <img src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=600&q=80" alt="Travel agency social media campaign" />
      <div class="portfolio-info">
        <h4>Travel Agency Campaign</h4>
        <p>Boosted bookings by 40% with an integrated digital marketing campaign.</p>
      </div>
    </div>
  </div>
</section>

<section class="about" id="about">
  <div class="container">
    <div class="about-text">
      <h3>About BrightWave Agency</h3>
      <p>Founded in 2010, BrightWave Agency has been delivering creative digital solutions for businesses of all sizes. Our passionate team of designers, developers, and strategists transform ideas into engaging online experiences, driving measurable growth and lasting impact. We believe in collaboration, innovation, and best-in-class service to help your brand shine in the digital world.</p>
    </div>
    <div class="about-img">
      <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=600&q=80" alt="BrightWave team working together" />
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <h3>Contact Us</h3>
  <form onsubmit="event.preventDefault(); alert('Thank you for reaching out! We will get back to you soon.'); this.reset();">
    <div class="form-control">
      <label for="name">Name *</label>
      <input id="name" type="text" placeholder="Your full name" required />
    </div>
    <div class="form-control">
      <label for="email">Email *</label>
      <input id="email" type="email" placeholder="Your email address" required />
    </div>
    <div class="form-control">
      <label for="message">Message *</label>
      <textarea id="message" placeholder="Your message" required></textarea>
    </div>
    <button type="submit">Send Message</button>
  </form>
</section>

<footer>
  &copy; 2024 BrightWave Agency - All rights reserved.
</footer>
</body>
</html>


