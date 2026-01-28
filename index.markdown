---
layout: default
---

<div class="minimal-landing-full">
  <a href="{{ '/software/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/software.jpg' | relative_url }}" alt="Software">
    <span>Software</span>
  </a>
  <a href="{{ '/engineering/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/engineering.jpg' | relative_url }}" alt="Engineering">
    <span>Engineering</span>
  </a>
  <a href="{{ '/leathercraft/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/leathercraft.jpg' | relative_url }}" alt="Leathercraft">
    <span>Leathercraft</span>
  </a>
</div>

<section class="about-section">
  <div class="about-container">
    <div class="about-image">
      <img src="{{ '/assets/images/profile.jpg' | relative_url }}" alt="Elense Studio Profile">
    </div>
    <div class="about-content">
      <h2>O Elense Studio</h2>
      <p>
        ASD Witaj w Elense Studio. Jestem pasjonatem tworzenia, łączącym świat nowoczesnych technologii z tradycyjnym rzemiosłem. 
        Moja praca to fuzja inżynieryjnej precyzji, innowacyjnego oprogramowania i duszy zawartej w ręcznie robionych wyrobach skórzanych. 
        Każdy projekt to nowa historia, którą staram się opowiedzieć poprzez jakość i dbałość o detal.
      </p>
      <div class="social-links">
        <a href="https://github.com/elense" target="_blank">GitHub</a>
        <a href="https://instagram.com/elense_leathercraft" target="_blank">Instagram</a>
        <a href="https://linkedin.com/in/elense" target="_blank">LinkedIn</a>
      </div>
    </div>
  </div>
</section>

<style>
/* Reset some default theme spacing for the landing page */
.page-content {
  padding: 0 !important;
}
.page-content .wrapper {
  max-width: 100% !important;
  padding: 0 !important;
  margin: 0 !important;
}
.site-header, .site-footer {
  display: none;
}

.minimal-landing-full {
  display: flex;
  justify-content: center;
  align-items: stretch;
  height: 100vh;
  gap: 0;
  padding: 0;
  margin: 0;
}

.landing-item {
  flex: 1;
  position: relative;
  overflow: hidden;
  text-decoration: none;
  transition: flex 0.5s ease;
}

.landing-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease, filter 0.5s ease;
  filter: grayscale(80%);
}

.landing-item span {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 2.5rem;
  font-weight: 300;
  text-transform: uppercase;
  letter-spacing: 4px;
  text-shadow: 0 0 20px rgba(0,0,0,0.5);
  z-index: 10;
  pointer-events: none;
  transition: font-size 0.5s ease;
}

.landing-item:hover {
  flex: 1.2;
}

.landing-item:hover img {
  transform: scale(1.05);
  filter: grayscale(0%);
}

.landing-item:hover span {
  font-size: 3rem;
  font-weight: 400;
}

@media (max-width: 768px) {
  .minimal-landing-full {
    flex-direction: column;
  }
  .landing-item {
    width: 100%;
  }
  .landing-item span {
    font-size: 1.8rem;
  }
}

.about-section {
  padding: 80px 20px;
  background-color: #f9f9f9;
  color: #333;
}

.about-container {
  max-width: 1400px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 80px;
}

.about-image {
  flex: 0 0 300px;
}

.about-image img {
  width: 100%;
  height: 300px;
  object-fit: cover;
  border-radius: 4px;
  filter: grayscale(100%);
  transition: filter 0.5s ease;
}

.about-container:hover .about-image img {
  filter: grayscale(0%);
}

.about-content {
  flex: 1;
}

.about-content h2 {
  font-size: 2rem;
  font-weight: 300;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 20px;
  border-bottom: 1px solid #ddd;
  padding-bottom: 10px;
}

.about-content p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #666;
  margin-bottom: 30px;
}

.social-links {
  display: flex;
  gap: 20px;
}

.social-links a {
  color: #333;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: color 0.3s ease;
  border: 1px solid #333;
  padding: 8px 16px;
}

.social-links a:hover {
  background-color: #333;
  color: #fff;
}

@media (max-width: 768px) {
  .about-container {
    flex-direction: column;
    text-align: center;
    gap: 30px;
  }
  .about-image {
    flex: 0 0 auto;
    width: 200px;
    margin: 0 auto;
  }
  .about-image img {
    height: 200px;
    border-radius: 50%;
  }
  .social-links {
    justify-content: center;
  }
}
</style>
