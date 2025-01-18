<template>
  <div class="current-products-section">
    <div class="section-header">
      <h2 class="section-title">Current Products</h2>
      <p class="section-subtitle">
        Innovative solutions powered by BioShuttle technology, available in market
      </p>
    </div>

    <div class="products-list">
      <!-- Weight Management Product -->
      <div class="product-card featured">
        <div class="product-image">
          <div class="image-placeholder">
            <svg class="product-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <circle cx="12" cy="12" r="10" stroke-width="2"/>
              <path d="M8 12L11 15L16 9" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </div>
        </div>
        
        <div class="product-content">
          <div class="product-header">
            <div class="product-badges">
              <span class="badge success">Available</span>
              <span class="badge market">UK Market</span>
            </div>
            <h3>Weight Management Solution</h3>
            <p class="product-description">
              Revolutionary diet formulation leveraging BioShuttle's enhanced bioavailability
              for optimal results with lower dosing requirements.
            </p>
          </div>

          <div class="product-details">
            <div class="detail-group">
              <h4>Key Features</h4>
              <ul class="feature-list">
                <li>Enhanced nutrient absorption</li>
                <li>Reduced dosage requirements</li>
                <li>Improved efficiency</li>
                <li>Consistent results</li>
              </ul>
            </div>

            <div class="detail-group">
              <h4>Market Performance</h4>
              <div class="performance-metrics">
                <div class="metric">
                  <span class="metric-value">4+</span>
                  <span class="metric-label">Months in Market</span>
                </div>
                <div class="metric">
                  <span class="metric-value">↗️</span>
                  <span class="metric-label">Sales Growth</span>
                </div>
                <div class="metric">
                  <span class="metric-value">UK</span>
                  <span class="metric-label">Distribution</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Pain Relief Product -->
      <div class="product-card">
        <div class="product-image">
          <div class="image-placeholder">
            <svg class="product-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L12 3l-.75.75a6 6 0 0 0-8.49 8.49l9.24 9.24L21.24 12.24z" stroke-width="2"/>
            </svg>
          </div>
        </div>

        <div class="product-content">
          <div class="product-header">
            <div class="product-badges">
              <span class="badge new">New Launch</span>
              <span class="badge market">US Market</span>
            </div>
            <h3>Pain Relief Solution</h3>
            <p class="product-description">
              Advanced pain management formulation utilizing targeted delivery for enhanced
              efficacy and reduced side effects.
            </p>
          </div>

          <div class="product-details">
            <div class="detail-group">
              <h4>Key Features</h4>
              <ul class="feature-list">
                <li>Targeted delivery</li>
                <li>Rapid onset</li>
                <li>Extended duration</li>
                <li>Minimal side effects</li>
              </ul>
            </div>

            <div class="detail-group">
              <h4>Market Status</h4>
              <div class="performance-metrics">
                <div class="metric">
                  <span class="metric-value">New</span>
                  <span class="metric-label">Launch Status</span>
                </div>
                <div class="metric">
                  <span class="metric-value">OTC</span>
                  <span class="metric-label">Category</span>
                </div>
                <div class="metric">
                  <span class="metric-value">US</span>
                  <span class="metric-label">Market</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Intimacy Product -->
      <div class="product-card">
        <div class="product-image">
          <div class="image-placeholder">
            <svg class="product-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z" stroke-width="2"/>
            </svg>
          </div>
        </div>

        <div class="product-content">
          <div class="product-header">
            <div class="product-badges">
              <span class="badge new">New Launch</span>
              <span class="badge market">US Market</span>
            </div>
            <h3>Intimate Wellness Solution</h3>
            <p class="product-description">
              Innovative formulation addressing postmenopausal intimacy concerns through
              targeted delivery and enhanced absorption.
            </p>
          </div>

          <div class="product-details">
            <div class="detail-group">
              <h4>Key Features</h4>
              <ul class="feature-list">
                <li>Enhanced absorption</li>
                <li>Targeted action</li>
                <li>Gentle formulation</li>
                <li>Long-lasting effects</li>
              </ul>
            </div>

            <div class="detail-group">
              <h4>Market Status</h4>
              <div class="performance-metrics">
                <div class="metric">
                  <span class="metric-value">New</span>
                  <span class="metric-label">Launch Status</span>
                </div>
                <div class="metric">
                  <span class="metric-value">Wellness</span>
                  <span class="metric-label">Category</span>
                </div>
                <div class="metric">
                  <span class="metric-value">US</span>
                  <span class="metric-label">Market</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// No dynamic logic required for this component
</script>

<style scoped>
.current-products-section {
  padding: 2rem 0;
}

.section-header {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 4rem;
}

.section-title {
  color: #1A365D;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.section-subtitle {
  color: #4A5568;
  font-size: 1.25rem;
  line-height: 1.6;
}

.products-list {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.product-card {
  background: white;
  border-radius: 16px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  display: grid;
  grid-template-columns: 200px 1fr;
  transition: transform 0.3s ease;
}

.product-card:hover {
  transform: translateY(-5px);
}

.product-card.featured {
  border: 2px solid #4299E1;
}

.product-image {
  background: #F7FAFC;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

.image-placeholder {
  width: 100px;
  height: 100px;
  background: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4299E1;
}

.product-icon {
  width: 48px;
  height: 48px;
}

.product-content {
  padding: 2rem;
}

.product-badges {
  display: flex;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

.badge {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 500;
}

.badge.success {
  background: #48BB78;
  color: white;
}

.badge.new {
  background: #4299E1;
  color: white;
}

.badge.market {
  background: #EDF2F7;
  color: #2D3748;
}

.product-header h3 {
  color: #2D3748;
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.product-description {
  color: #4A5568;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.product-details {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}

.detail-group h4 {
  color: #2D3748;
  font-size: 1.125rem;
  margin-bottom: 1rem;
}

.feature-list {
  list-style: none;
  padding: 0;
}

.feature-list li {
  color: #4A5568;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
}

.feature-list li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

.performance-metrics {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.metric {
  text-align: center;
}

.metric-value {
  display: block;
  font-size: 1.25rem;
  font-weight: 600;
  color: #2D3748;
  margin-bottom: 0.25rem;
}

.metric-label {
  font-size: 0.875rem;
  color: #718096;
}

@media (max-width: 1024px) {
  .product-card {
    grid-template-columns: 1fr;
  }

  .product-image {
    padding: 1.5rem;
  }

  .product-details {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .performance-metrics {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .product-content {
    padding: 1.5rem;
  }

  .performance-metrics {
    grid-template-columns: 1fr;
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
}
</style>