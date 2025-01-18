// pages/Index.vue
<template>
  <Layout>
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <div class="container">
        <div class="hero-content">
          <h1 class="hero-title">
            <span class="highlight">Revolutionary</span>
            Drug Delivery Platform
          </h1>
          <p class="hero-subtitle">
            Transform therapeutic compound delivery through BioShuttle's groundbreaking 
            stabilized liposome technology
          </p>
          <div class="hero-cta">
            <g-link to="/technology" class="btn btn-primary">
              Discover Our Technology
            </g-link>
            <g-link to="/contact" class="btn btn-secondary">
              Partner With Us
            </g-link>
          </div>
        </div>
      </div>
      <div class="hero-wave">
        <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 0L48 8.875C96 17.75 192 35.5 288 44.375C384 53.25 480 53.25 576 44.375C672 35.5 768 17.75 864 26.625C960 35.5 1056 71 1152 80C1248 89 1344 71 1392 62.125L1440 53.25V120H1392C1344 120 1248 120 1152 120C1056 120 960 120 864 120C768 120 672 120 576 120C480 120 384 120 288 120C192 120 96 120 48 120H0V0Z" fill="white"/>
        </svg>
      </div>
    </section>

    <!-- Key Benefits Section -->
    <section class="benefits">
      <div class="container">
        <h2 class="section-title">Transforming Drug Delivery</h2>
        <div class="benefits-grid">
          <div class="benefit-card">
            <div class="benefit-icon">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                <path d="M20 12V8H6a2 2 0 100 4h14v4H6a6 6 0 110-12h14v4" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <h3>Enhanced Bioavailability</h3>
            <p>Up to 50,000-fold lower dosing requirements with our proprietary technology</p>
          </div>
          <div class="benefit-card">
            <div class="benefit-icon">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke-width="2"/>
                <path d="M12 16V12M12 8H12.01" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>
            <h3>Exceptional Stability</h3>
            <p>Two-year shelf life at room temperature, surpassing traditional solutions</p>
          </div>
          <div class="benefit-card">
            <div class="benefit-icon">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                <path d="M5 3V7M3 5H7M6 17V21M4 19H8M13 3L15.2857 9.85714L21 12L15.2857 14.1429L13 21L10.7143 14.1429L5 12L10.7143 9.85714L13 3Z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <h3>Breakthrough Innovation</h3>
            <p>Revolutionary blood-brain barrier penetration capabilities</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Technology Overview -->
    <section class="technology">
      <div class="container">
        <h2 class="section-title">BioShuttle Platform</h2>
        <div class="tech-content">
          <div class="tech-visual">
            <!-- Replace with actual technology visualization -->
            <div class="tech-placeholder">
              <svg class="molecule-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                <circle cx="12" cy="12" r="3" stroke-width="2"/>
                <path d="M3 9L6 12M6 12L3 15M6 12H18M18 12L21 9M18 12L21 15" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>
          </div>
          <div class="tech-info">
            <h3>Versatile Drug Delivery System</h3>
            <p>Our proprietary stabilized liposomes transform the delivery of therapeutic compounds, offering:</p>
            <ul class="tech-features">
              <li>Potent and safe delivery mechanism</li>
              <li>Cost-effective solution</li>
              <li>Consistent performance</li>
              <li>Non-invasive administration</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Proof of Concept -->
    <section class="proof-concept">
      <div class="container">
        <h2 class="section-title">Proven Success</h2>
        <p class="section-subtitle">Five groundbreaking proof-of-concept treatments</p>
        <div class="concept-grid">
          <div class="concept-card">
            <div class="concept-icon">💪</div>
            <h4>Athletic Performance</h4>
            <p>Enhanced recovery and performance optimization</p>
          </div>
          <div class="concept-card">
            <div class="concept-icon">🌙</div>
            <h4>Sleep & Anxiety</h4>
            <p>Innovative solutions for anxiety-induced insomnia</p>
          </div>
          <div class="concept-card">
            <div class="concept-icon">❤️</div>
            <h4>Intimacy</h4>
            <p>Revolutionary postmenopausal wellness solutions</p>
          </div>
          <div class="concept-card">
            <div class="concept-icon">🎯</div>
            <h4>Pain Management</h4>
            <p>Effective relief with reduced side effects</p>
          </div>
          <div class="concept-card">
            <div class="concept-icon">⚖️</div>
            <h4>Weight Management</h4>
            <p>Successful market presence in the UK</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
      <div class="container">
        <h2>Ready to Transform Drug Delivery?</h2>
        <p>Partner with us to unlock the full potential of your therapeutic agents</p>
        <g-link to="/contact" class="btn btn-primary btn-large">
          Start the Conversation
        </g-link>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'BioShuttle - Revolutionary Drug Delivery Platform'
  }
}
</script>

<style scoped>
.hero {
  position: relative;
  min-height: 100vh;
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  color: white;
  padding: 120px 0 160px;
  overflow: hidden;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('/images/molecule-pattern.png') repeat;
  opacity: 0.1;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  position: relative;
}

.hero-content {
  max-width: 700px;
  margin: 0 auto;
  text-align: center;
}

.hero-title {
  font-size: 4rem;
  line-height: 1.2;
  margin-bottom: 1.5rem;
  font-weight: 700;
}

.highlight {
  color: #90cdf4;
}

.hero-subtitle {
  font-size: 1.5rem;
  line-height: 1.6;
  margin-bottom: 2.5rem;
  opacity: 0.9;
}

.hero-wave {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
}

.hero-cta {
  display: flex;
  gap: 1rem;
  justify-content: center;
}

.btn {
  display: inline-flex;
  align-items: center;
  padding: 1rem 2rem;
  border-radius: 8px;
  font-weight: 600;
  transition: all 0.3s ease;
  text-decoration: none;
}

.btn-primary {
  background: #4299e1;
  color: white;
}

.btn-primary:hover {
  background: #2b6cb0;
  transform: translateY(-2px);
}

.btn-secondary {
  background: transparent;
  border: 2px solid white;
  color: white;
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.benefits {
  padding: 100px 0;
  background: white;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  color: #2d3748;
  margin-bottom: 3rem;
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
}

.benefit-card {
  padding: 2rem;
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.benefit-card:hover {
  transform: translateY(-5px);
}

.benefit-icon {
  width: 64px;
  height: 64px;
  margin-bottom: 1.5rem;
  color: #4299e1;
}

.icon {
  width: 100%;
  height: 100%;
}

.technology {
  padding: 100px 0;
  background: #f7fafc;
}

.tech-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.tech-visual {
  aspect-ratio: 1;
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
}

.molecule-icon {
  width: 120px;
  height: 120px;
  color: #4299e1;
}

.tech-features {
  list-style: none;
  padding: 0;
  margin: 2rem 0 0;
}

.tech-features li {
  margin-bottom: 1rem;
  padding-left: 2rem;
  position: relative;
}

.tech-features li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299e1;
}

.proof-concept {
  padding: 100px 0;
  background: white;
}

.section-subtitle {
  text-align: center;
  font-size: 1.25rem;
  color: #4a5568;
  margin-bottom: 3rem;
}

.concept-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 2rem;
}

.concept-card {
  text-align: center;
  padding: 2rem;
  background: #f7fafc;
  border-radius: 12px;
  transition: transform 0.3s ease;
}

.concept-card:hover {
  transform: translateY(-5px);
}

.concept-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.cta {
  padding: 100px 0;
  background: linear-gradient(135deg, #2c5282 0%, #1a365d 100%);
  color: white;
  text-align: center;
}

.btn-large {
  padding: 1.25rem 2.5rem;
  font-size: 1.25rem;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 3rem;
  }

  .hero-subtitle {
    font-size: 1.25rem;
  }

  .tech-content {
    grid-template-columns: 1fr;
  }

  .hero-cta {
    flex-direction: column;
  }

  .btn {
    width: 100%;
    justify-content: center;
  }
}
</style>