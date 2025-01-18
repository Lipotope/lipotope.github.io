// components/technology/PlatformFeatures.vue
<template>
  <div class="platform-features">
    <div class="section-header">
      <h2 class="section-title">Platform Capabilities</h2>
      <p class="section-subtitle">
        BioShuttle's versatile technology enables breakthrough applications across multiple therapeutic areas
      </p>
    </div>

    <div class="features-grid">
      <!-- Gene Therapy -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z" stroke-width="2"/>
              <path d="M8 12H16M12 8V16" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Gene Therapy</h3>
          <p>Safe delivery of DNA, RNA, and oligonucleotides directly to the cell nucleus</p>
          <ul class="feature-details">
            <li>Efficient transfection</li>
            <li>Nuclear targeting</li>
            <li>Reduced cytotoxicity</li>
          </ul>
        </div>
      </div>

      <!-- Cancer Therapy -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M20.24 12.24a6 6 0 0 0-8.49-8.49L12 3l-.75.75a6 6 0 0 0-8.49 8.49l9.24 9.24L21.24 12.24z" stroke-width="2"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Cancer Therapy</h3>
          <p>Development of highly cytotoxic drugs with improved therapeutic indices</p>
          <ul class="feature-details">
            <li>Targeted delivery</li>
            <li>Reduced side effects</li>
            <li>Enhanced efficacy</li>
          </ul>
        </div>
      </div>

      <!-- Brain Drug Delivery -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M12 15C15.866 15 19 11.866 19 8C19 4.13401 15.866 1 12 1C8.13401 1 5 4.13401 5 8C5 11.866 8.13401 15 12 15Z" stroke-width="2"/>
              <path d="M12 15V23M8 19H16" stroke-width="2" stroke-linecap="round"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Brain Drug Delivery</h3>
          <p>Non-invasive penetration of the blood-brain barrier for CNS treatments</p>
          <ul class="feature-details">
            <li>BBB penetration</li>
            <li>Targeted distribution</li>
            <li>Neurological focus</li>
          </ul>
        </div>
      </div>

      <!-- Vaccines -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M3.85 8.62a4 4 0 0 1 4.78-4.77 4 4 0 0 1 6.74 0 4 4 0 0 1 4.78 4.77 4 4 0 0 1 0 6.76 4 4 0 0 1-4.78 4.77 4 4 0 0 1-6.74 0 4 4 0 0 1-4.78-4.77 4 4 0 0 1 0-6.76z" stroke-width="2"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Vaccines</h3>
          <p>Innovative antigen delivery system for enhanced immune response</p>
          <ul class="feature-details">
            <li>Sustained exposure</li>
            <li>No needles required</li>
            <li>Enhanced stability</li>
          </ul>
        </div>
      </div>

      <!-- Tissue Engineering -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M21 12a9 9 0 0 1-9 9m9-9a9 9 0 0 0-9-9m9 9H3m9 9a9 9 0 0 1-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 0 1 9-9" stroke-width="2"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Tissue Engineering</h3>
          <p>Targeted delivery of growth and differentiation factors</p>
          <ul class="feature-details">
            <li>Controlled release</li>
            <li>Local delivery</li>
            <li>Tissue regeneration</li>
          </ul>
        </div>
      </div>

      <!-- Immunomodulation -->
      <div class="feature-card">
        <div class="feature-icon">
          <div class="icon-circle">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
              <path d="M8.56 2.9A7 7 0 0 1 19 9v4m-2.18 8.67A7 7 0 0 1 5 16v-4m2.18-8.67A7 7 0 0 0 5 12v4m16-4a7 7 0 0 1-7 7" stroke-width="2"/>
            </svg>
          </div>
        </div>
        <div class="feature-content">
          <h3>Immunomodulation</h3>
          <p>Precise control of immune responses for various conditions</p>
          <ul class="feature-details">
            <li>Autoimmune therapy</li>
            <li>Transplant support</li>
            <li>Cancer immunotherapy</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// No dynamic logic required for this component
</script>

<style scoped>
.platform-features {
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

.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.feature-card {
  background: white;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  display: flex;
  flex-direction: column;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-icon {
  margin-bottom: 1.5rem;
}

.icon-circle {
  width: 48px;
  height: 48px;
  background: #EBF8FF;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4299E1;
}

.icon {
  width: 24px;
  height: 24px;
}

.feature-content h3 {
  color: #2D3748;
  font-size: 1.25rem;
  margin-bottom: 0.75rem;
}

.feature-content p {
  color: #4A5568;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.feature-details {
  list-style: none;
  padding: 0;
  margin-top: auto;
}

.feature-details li {
  color: #718096;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
}

.feature-details li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

@media (max-width: 1024px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .section-title {
    font-size: 2rem;
  }
}

@media (max-width: 768px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
  
  .platform-features {
    padding: 1rem 0;
  }
  
  .feature-card {
    padding: 1.5rem;
  }
}
</style>