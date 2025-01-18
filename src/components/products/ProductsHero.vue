// components/products/ProductsHero.vue
<template>
  <section class="products-hero">
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">
          Market-Ready Solutions
        </h1>
        <p class="hero-subtitle">
          Discover our innovative products powered by BioShuttle technology
        </p>
      </div>

      <div class="products-showcase">
        <div class="product-highlight active">
          <div class="product-status">
            <span class="status-badge success">Available Now</span>
            <span class="market-badge">UK Market</span>
          </div>
          <h2>Weight Management Solution</h2>
          <p class="highlight-description">
            Revolutionary diet formulation with exponentially growing sales in the United Kingdom
          </p>
          <div class="highlight-metrics">
            <div class="metric">
              <span class="metric-value">4+</span>
              <span class="metric-label">Months in Market</span>
            </div>
            <div class="metric">
              <span class="metric-value">↗️</span>
              <span class="metric-label">Growing Sales</span>
            </div>
            <div class="metric">
              <span class="metric-value">UK</span>
              <span class="metric-label">Distribution</span>
            </div>
          </div>
        </div>

        <div class="recent-launches">
          <h3>Recent Launches</h3>
          <div class="launch-cards">
            <div class="launch-card">
              <div class="card-content">
                <div class="status-badge new">New Launch</div>
                <h4>Pain Relief</h4>
                <p>Advanced formulation for enhanced pain management</p>
                <span class="market">US Market</span>
              </div>
            </div>

            <div class="launch-card">
              <div class="card-content">
                <div class="status-badge new">New Launch</div>
                <h4>Intimate Wellness</h4>
                <p>Innovative solution for postmenopausal intimacy</p>
                <span class="market">US Market</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="product-navigation">
        <div class="nav-links">
          <a href="#current-products" class="nav-link active">
            Current Products
          </a>
          <a href="#pipeline" class="nav-link">
            Product Pipeline
          </a>
          <a href="#development" class="nav-link">
            Development Process
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProductsHero'
}
</script>

<style scoped>
.products-hero {
  padding: 6rem 0;
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  color: white;
  position: relative;
}

.hero-content {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 4rem;
}

.hero-title {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.hero-subtitle {
  font-size: 1.25rem;
  line-height: 1.6;
  opacity: 0.9;
}

.products-showcase {
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  gap: 2rem;
  margin-bottom: 4rem;
}

.product-highlight {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 2rem;
  backdrop-filter: blur(10px);
}

.product-status {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.status-badge {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 500;
}

.status-badge.success {
  background: #48BB78;
  color: white;
}

.status-badge.new {
  background: #4299E1;
  color: white;
}

.market-badge {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  background: rgba(255, 255, 255, 0.2);
  font-size: 0.875rem;
}

.product-highlight h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.highlight-description {
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 2rem;
  opacity: 0.9;
}

.highlight-metrics {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  padding-top: 1.5rem;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}

.metric {
  text-align: center;
}

.metric-value {
  display: block;
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.metric-label {
  font-size: 0.875rem;
  opacity: 0.8;
}

.recent-launches {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.recent-launches h3 {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.launch-cards {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.launch-card {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  padding: 1.5rem;
  backdrop-filter: blur(10px);
}

.launch-card h4 {
  font-size: 1.25rem;
  margin: 1rem 0 0.5rem;
}

.launch-card p {
  opacity: 0.9;
  margin-bottom: 1rem;
  line-height: 1.5;
}

.market {
  font-size: 0.875rem;
  opacity: 0.8;
}

.product-navigation {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 50px;
  padding: 0.5rem;
  max-width: 600px;
  margin: 0 auto;
}

.nav-links {
  display: flex;
  justify-content: space-between;
  gap: 1rem;
}

.nav-link {
  color: white;
  text-decoration: none;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  transition: all 0.3s ease;
  font-weight: 500;
}

.nav-link:hover {
  background: rgba(255, 255, 255, 0.1);
}

.nav-link.active {
  background: #4299E1;
}

@media (max-width: 1024px) {
  .products-showcase {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .hero-title {
    font-size: 2.5rem;
  }
}

@media (max-width: 768px) {
  .products-hero {
    padding: 4rem 0;
  }

  .hero-title {
    font-size: 2rem;
  }

  .product-highlight h2 {
    font-size: 1.75rem;
  }

  .highlight-metrics {
    grid-template-columns: 1fr;
    text-align: left;
  }

  .metric {
    text-align: left;
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .metric-value {
    margin-bottom: 0;
  }

  .nav-links {
    flex-direction: column;
  }

  .nav-link {
    text-align: center;
  }
}
</style>