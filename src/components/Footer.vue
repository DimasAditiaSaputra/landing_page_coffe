<script setup></script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>About Us</h3>
        <p>
          At Brew & Bliss, we serve artisanal coffee and desserts made with
          passion. Come sip the warmth of tradition blended with a modern twist.
        </p>
        <div class="social-icons">
          <a href="#"><i class="fab fa-facebook-f">f</i></a>
          <a href="#"><i class="fab fa-twitter">t</i></a>
          <a href="#"><i class="fab fa-instagram">in</i></a>
          <a href="#"><i class="fab fa-linkedin-in">li</i></a>
        </div>
      </div>

      <div class="footer-section">
        <h3>Quick Links</h3>
        <ul class="footer-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">Menu</a></li>
          <li><a href="#">Story</a></li>
          <li><a href="#">Brew Tips</a></li>
          <li><a href="#">Order</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>

      <div class="footer-section">
        <h3>Contact Us</h3>
        <div class="contact-info">
          <div class="contact-item">
            <i class="fas fa-map-marker-alt">📍</i>
            <span>42 Roast St, Bean Town</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-phone">📞</i>
            <span>+62 812 3456 7890</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-envelope">✉️</i>
            <span>hello@brewbliss.com</span>
          </div>
        </div>
      </div>

      <div class="footer-section">
        <h3>Newsletter</h3>
        <p>
          Get exclusive offers and coffee brewing tips straight to your inbox.
        </p>
        <form class="subscribe-form">
          <input type="email" placeholder="Your email" />
          <button type="submit">Join</button>
        </form>
      </div>
    </div>

    <div class="footer-bottom">
      <p>
        <span>&copy; 2025 Brew & Bliss. Made with ☕</span>
        <span class="footer-menu">
          <a href="#">Privacy</a>
          <a href="#">Terms</a>
          <a href="#">Cookies</a>
        </span>
      </p>
    </div>
  </footer>
</template>

<style>
.footer {
  background: linear-gradient(135deg, #3e2c26 0%, #231710 100%);
  color: #f5f0eb;
  font-family: "Georgia", serif;
  padding: 0;
  width: 100%;
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 3rem 2rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.footer-section h3 {
  color: #f3d9c1;
  font-size: 1.4rem;
  margin-bottom: 1rem;
  font-weight: 600;
  border-bottom: 2px solid #d2a679;
  padding-bottom: 0.5rem;
}

.footer-section p {
  color: #d6c6b8;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.footer-links {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin-bottom: 10px;
}

.footer-links a {
  color: #d6c6b8;
  text-decoration: none;
  transition: color 0.3s ease;
  font-size: 0.95rem;
}

.footer-links a:hover {
  color: #e0b084;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 10px;
  color: #d6c6b8;
  font-size: 0.95rem;
}

.social-icons {
  display: flex;
  gap: 12px;
  margin-top: 1rem;
}

.social-icons a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  background-color: #6b4f4f;
  color: #fff;
  transition: all 0.3s ease;
  text-decoration: none;
  font-weight: bold;
}

.social-icons a:hover {
  background-color: #d2a679;
  transform: translateY(-3px);
}

.footer-bottom {
  background-color: #1c120d;
  padding: 1rem 2rem;
  text-align: center;
  font-size: 0.85rem;
  color: #bcae9c;
}

.footer-bottom p {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-menu {
  display: flex;
  gap: 1.2rem;
}

.footer-menu a {
  color: #bcae9c;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-menu a:hover {
  color: #e0b084;
}

.subscribe-form {
  display: flex;
  margin-top: 1rem;
}

.subscribe-form input {
  flex: 1;
  padding: 10px 14px;
  border: none;
  background-color: #5c4033;
  color: #fff;
  border-radius: 4px 0 0 4px;
  font-size: 0.9rem;
}

.subscribe-form input::placeholder {
  color: #c8b8aa;
}

.subscribe-form button {
  padding: 0 16px;
  background-color: #d2a679;
  color: white;
  border: none;
  border-radius: 0 4px 4px 0;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.subscribe-form button:hover {
  background-color: #b38867;
}

/* Responsive tweaks */
@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .footer-section h3 {
    border-bottom: none;
  }

  .contact-item,
  .social-icons {
    justify-content: center;
  }

  .footer-bottom p {
    flex-direction: column;
  }

  .footer-menu {
    justify-content: center;
    margin-top: 1rem;
  }

  .subscribe-form {
    flex-direction: column;
    gap: 10px;
  }

  .subscribe-form input,
  .subscribe-form button {
    width: 100%;
    border-radius: 4px;
  }
}
</style>
