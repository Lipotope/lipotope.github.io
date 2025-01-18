// components/technology/TechnologyOverview.vue
<template>
  <section class="technology-overview">
    <div class="container">
      <div class="overview-grid">
        <!-- Left Column: Content -->
        <div class="overview-content">
          <h1 class="overview-title">
            BioShuttle Platform Technology
          </h1>
          <p class="overview-subtitle">
            A groundbreaking drug delivery platform utilizing proprietary stabilized liposomes
          </p>
          
          <div class="key-features">
            <div class="feature-item">
              <div class="feature-icon">
                <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                  <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke-width="2"/>
                  <path d="M7.5 12L10.5 15L16.5 9" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <div class="feature-content">
                <h3>Enhanced Bioavailability</h3>
                <p>Enables doses 1,000 to 50,000-fold lower than traditional delivery methods</p>
              </div>
            </div>

            <div class="feature-item">
              <div class="feature-icon">
                <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                  <path d="M12 15C15.866 15 19 11.866 19 8C19 4.13401 15.866 1 12 1C8.13401 1 5 4.13401 5 8C5 11.866 8.13401 15 12 15Z" stroke-width="2"/>
                  <path d="M12 15V23M8 19H16" stroke-width="2" stroke-linecap="round"/>
                </svg>
              </div>
              <div class="feature-content">
                <h3>Barrier Breaking</h3>
                <p>Overcomes the blood-brain barrier for targeted therapeutic delivery</p>
              </div>
            </div>

            <div class="feature-item">
              <div class="feature-icon">
                <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                  <path d="M12 8V12L15 15" stroke-width="2" stroke-linecap="round"/>
                  <circle cx="12" cy="12" r="10" stroke-width="2"/>
                </svg>
              </div>
              <div class="feature-content">
                <h3>Extended Stability</h3>
                <p>Up to two years shelf life at room temperature</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Right Column: Visual -->
        <div class="overview-visual">
          <div class="visual-container">
            <svg class="tech-diagram" viewBox="0 0 400 400" fill="none">
              <!-- Outer Circle -->
              <circle cx="200" cy="200" r="180" stroke="#4299e1" stroke-width="2" stroke-dasharray="8 8"/>
              
              <!-- Inner Circles representing liposome layers -->
              <circle cx="200" cy="200" r="140" stroke="#2b6cb0" stroke-width="3"/>
              <circle cx="200" cy="200" r="100" stroke="#2c5282" stroke-width="3"/>
              
              <!-- Center particle -->
              <circle cx="200" cy="200" r="40" fill="#1a365d"/>
              
              <!-- Decorative particles -->
              <circle cx="150" cy="150" r="8" fill="#4299e1"/>
              <circle cx="250" cy="250" r="8" fill="#4299e1"/>
              <circle cx="150" cy="250" r="8" fill="#4299e1"/>
              <circle cx="250" cy="150" r="8" fill="#4299e1"/>
              
              <!-- Connection lines -->
              <path d="M180 180L220 220" stroke="#4299e1" stroke-width="2"/>
              <path d="M180 220L220 180" stroke="#4299e1" stroke-width="2"/>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TechnologyOverview'
}
</script>

<style scoped>
.technology-overview {
  padding: 6rem 0;
  background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
}

.overview-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.overview-content {
  padding-right: 2rem;
}

.overview-title {
  font-size: 2.5rem;
  color: #1a365d;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.overview-subtitle {
  font-size: 1.25rem;
  color: #4a5568;
  margin-bottom: 3rem;
  line-height: 1.6;
}

.key-features {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.feature-item {
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
}

.feature-icon {
  flex-shrink: 0;
  width: 48px;
  height: 48px;
  background: #ebf8ff;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4299e1;
}

.icon {
  width: 24px;
  height: 24px;
}

.feature-content h3 {
  color: #2d3748;
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}

.feature-content p {
  color: #4a5568;
  line-height: 1.6;
}

.overview-visual {
  position: relative;
}

.visual-container {
  position: relative;
  padding-top: 100%; /* 1:1 Aspect Ratio */
}

.tech-diagram {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  animation: rotate 60s linear infinite;
}

@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

@media (max-width: 1024px) {
  .overview-grid {
    gap: 3rem;
  }
  
  .overview-title {
    font-size: 2rem;
  }
  
  .overview-subtitle {
    font-size: 1.125rem;
  }
}

@media (max-width: 768px) {
  .overview-grid {
    grid-template-columns: 1fr;
  }
  
  .overview-content {
    padding-right: 0;
  }
  
  .technology-overview {
    padding: 4rem 0;
  }
}
</style>