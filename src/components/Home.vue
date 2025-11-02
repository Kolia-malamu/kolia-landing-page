<script setup lang="ts">
import { onMounted } from 'vue';

function handleSubmit(event) {
  event.preventDefault();
  const email = event.target.querySelector('input').value;
  alert(`Merci pour votre intérêt ! Nous vous tiendrons informé à l'adresse : ${email}`);
  event.target.reset();
}

const scrollToSection = (hash: string) => {
  const target = document.querySelector(hash);
  if (target) {
    target.scrollIntoView({
      behavior: 'smooth',
      block: 'start'
    });
  }
};

// Ajouter les event listeners après le montage du composant
onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', (e) => {
      e.preventDefault();
      const href = anchor.getAttribute('href');
      if (href) {
        scrollToSection(href);
      }
    });
  });
});
</script>

<template>
  <header>
    <nav class="container">
      <div class="logo">🌱 Kolia Malamu</div>
      <ul class="nav-links">
        <li><a href="#concept">Concept</a></li>
        <li><a href="#avantages">Avantages</a></li>
        <li><a href="#fonctionnement">Fonctionnement</a></li>
        <li><a href="#rejoindre">Rejoindre</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-content container">
      <h1>Kolia Malamu</h1>
      <p class="tagline">Du producteur au consommateur, sans intermédiaire</p>
      <p>Découvrez une nouvelle façon de consommer : connectez-vous directement avec les producteurs locaux, connaissez l'origine de vos produits et créez du lien avec ceux qui nourrissent votre communauté.</p>
      <div class="cta-buttons">
        <a href="#rejoindre" class="btn btn-primary">Rejoindre la liste d'attente</a>
        <a href="#concept" class="btn btn-secondary">En savoir plus</a>
      </div>
    </div>
  </section>

  <section id="concept" class="features">
    <div class="container">
      <h2 class="section-title">Une plateforme qui change tout</h2>
      <p class="section-subtitle">Transparence, traçabilité et proximité au cœur de votre alimentation</p>

      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon">🌾</div>
          <h3>Produits locaux</h3>
          <p>Accédez directement aux produits frais de votre région. Connaissez la provenance exacte de ce que vous consommez.</p>
        </div>

        <div class="feature-card">
          <div class="feature-icon">💰</div>
          <h3>Prix justes</h3>
          <p>Des prix équitables pour tous : les producteurs sont rémunérés correctement, les consommateurs paient le juste prix.</p>
        </div>

        <div class="feature-card">
          <div class="feature-icon">🤝</div>
          <h3>Lien direct</h3>
          <p>Créez une relation authentique avec les producteurs. Découvrez leur histoire, leurs méthodes et leurs valeurs.</p>
        </div>

        <div class="feature-card">
          <div class="feature-icon">📱</div>
          <h3>Simple et accessible</h3>
          <p>Une application web et mobile intuitive pour acheter en quelques clics, disponible partout, à tout moment.</p>
        </div>

        <div class="feature-card">
          <div class="feature-icon">🔍</div>
          <h3>Transparence totale</h3>
          <p>Toutes les informations sur les produits : origine, méthodes de production, certification, et traçabilité complète.</p>
        </div>

        <div class="feature-card">
          <div class="feature-icon">🌍</div>
          <h3>Impact positif</h3>
          <p>Soutenez l'économie locale, réduisez votre empreinte carbone et participez à un modèle de consommation responsable.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="fonctionnement" class="how-it-works">
    <div class="container">
      <h2 class="section-title">Comment ça marche ?</h2>
      <p class="section-subtitle">Un circuit court en 3 étapes simples</p>

      <div class="steps">
        <div class="step">
          <div class="step-number">1</div>
          <h3>Découvrez</h3>
          <p>Parcourez les produits disponibles près de chez vous. Consultez les fiches détaillées avec photos, prix, et histoire du producteur.</p>
        </div>

        <div class="step">
          <div class="step-number">2</div>
          <h3>Commandez</h3>
          <p>Sélectionnez vos produits préférés et passez commande directement auprès du producteur en quelques clics.</p>
        </div>

        <div class="step">
          <div class="step-number">3</div>
          <h3>Récupérez</h3>
          <p>Retirez vos produits frais au point de collecte ou bénéficiez d'une livraison directe selon les options proposées.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="avantages" class="benefits">
    <div class="container">
      <h2 class="section-title">Des avantages pour tous</h2>

      <div class="benefits-split">
        <div class="benefit-section">
          <h3>👨‍🌾 Pour les producteurs</h3>
          <ul>
            <li>
              <span class="check-icon">✓</span>
              <span>Vendez directement sans intermédiaire et augmentez vos marges</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Valorisez votre travail et racontez votre histoire</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Accédez à une nouvelle clientèle locale fidèle</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Gérez facilement votre catalogue et vos commandes</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Recevez vos paiements rapidement et en toute sécurité</span>
            </li>
          </ul>
        </div>

        <div class="benefit-section">
          <h3>🛒 Pour les consommateurs</h3>
          <ul>
            <li>
              <span class="check-icon">✓</span>
              <span>Achetez des produits frais et locaux de qualité</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Connaissez l'origine exacte de vos aliments</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Payez le juste prix sans marges abusives</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Soutenez les producteurs de votre région</span>
            </li>
            <li>
              <span class="check-icon">✓</span>
              <span>Participez à une consommation responsable et durable</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <section id="rejoindre" class="cta-section">
    <div class="container">
      <h2>Prêt à rejoindre le mouvement ?</h2>
      <p>Inscrivez-vous à notre liste d'attente et soyez parmi les premiers à découvrir Kolia Malamu lors de notre lancement.</p>

      <form class="email-form" @submit="handleSubmit">
        <input type="email" placeholder="Votre adresse email" required>
        <button type="submit">Je m'inscris</button>
      </form>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 Kolia Malamu. Tous droits réservés.</p>
      <p style="margin-top: 0.5rem; opacity: 0.8;">🌱 Pour une consommation locale et responsable</p>
    </div>
  </footer>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #333;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header */
header {
  background: linear-gradient(135deg, #2d5016 0%, #4a7c2c 100%);
  color: white;
  padding: 1rem 0;
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: bold;
  letter-spacing: 1px;
}

.nav-links {
  display: flex;
  gap: 2rem;
  list-style: none;
}

.nav-links a {
  color: white;
  text-decoration: none;
  transition: opacity 0.3s;
}

.nav-links a:hover {
  opacity: 0.8;
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, #2d5016 0%, #4a7c2c 50%, #6b9b47 100%);
  color: white;
  padding: 150px 20px 100px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="2" fill="rgba(255,255,255,0.1)"/></svg>');
  opacity: 0.3;
}

.hero-content {
  position: relative;
  z-index: 1;
}

.hero h1 {
  font-size: 3.5rem;
  margin-bottom: 1rem;
  animation: fadeInUp 0.8s ease;
}

.hero .tagline {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  opacity: 0.95;
  animation: fadeInUp 0.8s ease 0.2s backwards;
}

.hero p {
  font-size: 1.2rem;
  max-width: 700px;
  margin: 0 auto 2.5rem;
  animation: fadeInUp 0.8s ease 0.4s backwards;
}

.cta-buttons {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
  animation: fadeInUp 0.8s ease 0.6s backwards;
}

.btn {
  padding: 15px 40px;
  font-size: 1.1rem;
  border: none;
  border-radius: 50px;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
  display: inline-block;
  font-weight: 600;
}

.btn-primary {
  background: white;
  color: #2d5016;
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background: white;
  color: #2d5016;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Features Section */
.features {
  padding: 100px 20px;
  background: #f8f9fa;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: #2d5016;
}

.section-subtitle {
  text-align: center;
  font-size: 1.2rem;
  color: #666;
  margin-bottom: 4rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 3rem;
  margin-top: 3rem;
}

.feature-card {
  background: white;
  padding: 2.5rem;
  border-radius: 15px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.08);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0,0,0,0.15);
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.feature-card h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: #2d5016;
}

/* How it works */
.how-it-works {
  padding: 100px 20px;
  background: white;
}

.steps {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
  margin-top: 4rem;
}

.step {
  text-align: center;
  position: relative;
}

.step-number {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #2d5016, #4a7c2c);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  font-weight: bold;
  margin: 0 auto 1.5rem;
  box-shadow: 0 5px 20px rgba(45, 80, 22, 0.3);
}

.step h3 {
  font-size: 1.3rem;
  margin-bottom: 1rem;
  color: #2d5016;
}

/* Benefits Split */
.benefits {
  padding: 100px 20px;
  background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
}

.benefits-split {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 4rem;
  margin-top: 4rem;
}

.benefit-section {
  background: white;
  padding: 3rem;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

.benefit-section h3 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #2d5016;
  display: flex;
  align-items: center;
  gap: 1rem;
}

.benefit-section ul {
  list-style: none;
}

.benefit-section li {
  padding: 1rem 0;
  border-bottom: 1px solid #e9ecef;
  display: flex;
  align-items: start;
  gap: 1rem;
}

.benefit-section li:last-child {
  border-bottom: none;
}

.check-icon {
  color: #4a7c2c;
  font-size: 1.5rem;
  flex-shrink: 0;
}

/* CTA Section */
.cta-section {
  padding: 100px 20px;
  background: linear-gradient(135deg, #2d5016 0%, #4a7c2c 100%);
  color: white;
  text-align: center;
}

.cta-section h2 {
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
}

.cta-section p {
  font-size: 1.2rem;
  margin-bottom: 2.5rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.email-form {
  display: flex;
  gap: 1rem;
  max-width: 500px;
  margin: 0 auto;
  flex-wrap: wrap;
  justify-content: center;
}

.email-form input {
  flex: 1;
  min-width: 250px;
  padding: 15px 20px;
  border: none;
  border-radius: 50px;
  font-size: 1rem;
}

.email-form button {
  padding: 15px 40px;
  background: white;
  color: #2d5016;
  border: none;
  border-radius: 50px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.email-form button:hover {
  transform: scale(1.05);
}

/* Footer */
footer {
  background: #1a2f0d;
  color: white;
  padding: 2rem 20px;
  text-align: center;
}

/* Responsive */
@media (max-width: 768px) {
  .hero h1 {
    font-size: 2.5rem;
  }

  .hero .tagline {
    font-size: 1.2rem;
  }

  .nav-links {
    display: none;
  }

  .benefits-split {
    grid-template-columns: 1fr;
  }

  .email-form {
    flex-direction: column;
  }

  .email-form input,
  .email-form button {
    width: 100%;
  }
}
</style>