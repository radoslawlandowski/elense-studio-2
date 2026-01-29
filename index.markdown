---
layout: default
---

<div class="minimal-landing-full">
  <a href="{{ '/software/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/software.jpg' | relative_url }}" alt="Software">
    <div class="landing-content">
      <span>Software</span>
      <p>Nowoczesne aplikacje webowe i mobilne</p>
    </div>
  </a>
  <a href="{{ '/engineering/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/engineering.jpg' | relative_url }}" alt="Engineering">
    <div class="landing-content">
      <span>Engineering</span>
      <p>Precyzyjne projekty mechaniczne i prototypowanie</p>
    </div>
  </a>
  <a href="{{ '/leathercraft/' | relative_url }}" class="landing-item">
    <img src="{{ '/assets/images/leathercraft.jpg' | relative_url }}" alt="Leathercraft">
    <div class="landing-content">
      <span>Leathercraft</span>
      <p>Tradycyjne rzemiosło w nowoczesnym wydaniu</p>
    </div>
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
  display: block;
}

.minimal-landing-full {
  display: flex;
  justify-content: center;
  align-items: stretch;
  height: calc(100vh - 80px);
  gap: 0;
  padding: 0;
  margin: 0;
}

.landing-item {
  flex: 1;
  position: relative;
  overflow: hidden;
  text-decoration: none;
  transition: flex 0.6s cubic-bezier(0.25, 1, 0.5, 1);
}

.landing-item::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(to bottom, rgba(0,0,0,0) 0%, rgba(0,0,0,0.6) 100%);
  z-index: 5;
  opacity: 0.6;
  transition: opacity 0.5s ease;
}

.landing-item:hover::after {
  opacity: 0.8;
}

.landing-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.8s cubic-bezier(0.25, 1, 0.5, 1);
}

.landing-content {
  position: absolute;
  bottom: 60px;
  left: 40px;
  right: 40px;
  color: white;
  z-index: 10;
  pointer-events: none;
  transition: transform 0.5s ease;
}

.landing-item span {
  display: block;
  font-size: 2.5rem;
  font-weight: 300;
  text-transform: uppercase;
  letter-spacing: 6px;
  margin-bottom: 10px;
  font-family: var(--font-serif);
}

.landing-content p {
  font-size: 1rem;
  font-weight: 300;
  letter-spacing: 1px;
  opacity: 0;
  transform: translateY(20px);
  transition: all 0.5s ease;
  margin: 0;
}

.landing-item:hover {
  flex: 1.5;
}

.landing-item:hover img {
  transform: scale(1.1);
}

.landing-item:hover .landing-content p {
  opacity: 1;
  transform: translateY(0);
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
