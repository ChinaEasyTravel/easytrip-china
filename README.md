index.html             ← Home + Services + Promo + Contact
styles.css            ← Basic responsive styles
script.js             ← For basic interactivity (form submission)
index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>EasyTrip China – Local Travel Services</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1>EasyTrip China</h1>
    <p>Your Local Drivers, Translators & Travel Assistants</p>
  </header>

  <section id="promo">
    <h2> First Booking Offer: 30%–50% OFF!</h2>
    <p>Get your trip started with amazing savings.</p>
    <a href="#contact" class="btn">Book Now</a>
  </section>

  <section id="services">
    <h2>Our Services</h2>
    <div class="service-card">
      <h3>Local Drivers</h3>
      <p>Professional, licensed, English-speaking drivers for airport rides, tours & transfers — from $30/day.</p>
    </div>
    <div class="service-card">
      <h3>Translators / Interpreters</h3>
      <p>Fluent in major languages for your business or travel needs — from $20/hour.</p>
    </div>
    <div class="service-card">
      <h3>Travel Assistants</h3>
      <p>Help with hotel check-ins, dining, tickets & emergency support — from $25/day.</p>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Our Consultant</h2>
    <p>We’re available 7 days a week, 9am–9pm CST.</p>
    <form id="contact-form">
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <input type="tel" name="phone" placeholder="Phone or WhatsApp" required />
      <textarea name="message" placeholder="Tell us about your trip..." required></textarea>
      <button type="submit">Get a Quote</button>
    </form>
    <div class="contact-info">
      <p> info@easytripchina.com</p>
      <p> +86‑135‑0000‑0000 (WhatsApp/Phone)</p>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 EasyTrip China</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
styles.css
body {
  font-family: sans-serif;
  line-height: 1.6;
  margin: 0;
  padding: 0;
  color: #333;
}
header, section, footer {
  padding: 1.5rem;
  margin: 0 auto;
  max-width: 800px;
}
header {
  background: #0078d4;
  color: white;
  text-align: center;
  padding: 2rem 1rem;
}
#promo {
  background: #f8f8f8;
  text-align: center;
  margin-top: 1rem;
}
.btn {
  display: inline-block;
  background: #0078d4;
  color: white;
  padding: .7rem 1.2rem;
  text-decoration: none;
  border-radius: 4px;
  margin-top: .5rem;
}
.service-card {
  background: #eef;
  padding: 1rem;
  margin: 1rem 0;
  border-radius: 4px;
}
form {
  display: flex;
  flex-direction: column;
}
form input, form textarea, form button {
  margin: .5rem 0;
  padding: .8rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}
form button {
  background: #0078d4;
  color: white;
  border: none;
  cursor: pointer;
}
form button:hover {
  background: #005fa1;
}
.contact-info {
  margin-top: 1rem;
}
footer {
  text-align: center;
  font-size: .9rem;
  color: #777;
}
@media (min-width: 600px) {
  .service-card {
    display: inline-block;
    width: 30%;
    vertical-align: top;
    margin-right: 3.3%;
  }
  .service-card:last-child {
    margin-right: 0;
  }
}
script.js
document.getElementById('contact-form').addEventListener('submit', function(e) {
  e.preventDefault();
  alert('Thanks for your inquiry! Our consultant will be in touch within 24 hours.');
  this.reset();
});
