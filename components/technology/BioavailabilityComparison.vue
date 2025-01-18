// components/technology/BioavailabilityComparison.vue
<template>
  <div class="bioavailability-section">
    <div class="section-header">
      <h2 class="section-title">Enhanced Bioavailability</h2>
      <p class="section-subtitle">
        Comparative analysis showing BioShuttle's dramatic improvement in drug delivery efficiency
      </p>
    </div>

    <div class="comparison-container">
      <div class="comparison-tabs">
        <button 
          v-for="(category, index) in categories" 
          :key="index"
          class="tab-button"
          :class="{ active: activeTab === index }"
          @click="activeTab = index"
        >
          {{ category.name }}
        </button>
      </div>

      <div class="comparison-content">
        <div class="comparison-cards">
          <div class="comparison-card traditional">
            <h3>Traditional Delivery</h3>
            <div class="dosage-value">100%</div>
            <p class="dosage-label">Standard Dosage</p>
            <ul class="feature-list">
              <li>Standard bioavailability</li>
              <li>Higher API requirements</li>
              <li>Increased side effects risk</li>
            </ul>
          </div>

          <div class="comparison-card bioshuttle">
            <div class="improvement-badge">
              Up to 50,000x More Efficient
            </div>
            <h3>BioShuttle™ Delivery</h3>
            <div class="dosage-value">0.002%</div>
            <p class="dosage-label">Required Dosage</p>
            <ul class="feature-list">
              <li>Enhanced bioavailability</li>
              <li>Minimal API requirements</li>
              <li>Reduced side effects</li>
            </ul>
          </div>
        </div>

        <div class="key-metrics">
          <div class="metric-box">
            <div class="metric-icon">↓</div>
            <div class="metric-details">
              <div class="metric-value">50,000x</div>
              <div class="metric-label">Lower Dosing</div>
            </div>
          </div>

          <div class="metric-box">
            <div class="metric-icon">↑</div>
            <div class="metric-details">
              <div class="metric-value">95%+</div>
              <div class="metric-label">Delivery Efficiency</div>
            </div>
          </div>

          <div class="metric-box">
            <div class="metric-icon">💰</div>
            <div class="metric-details">
              <div class="metric-value">80%+</div>
              <div class="metric-label">Cost Reduction</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const activeTab = ref(0)
const categories = [
  { name: 'General Comparison' },
  { name: 'Brain Delivery' },
  { name: 'Tissue Targeting' }
]
</script>

<style scoped>
.bioavailability-section {
  padding: 2rem 0;
}

.section-header {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 3rem;
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

.comparison-container {
  background: white;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.comparison-tabs {
  display: flex;
  gap: 1rem;
  margin-bottom: 2rem;
  justify-content: center;
}

.tab-button {
  padding: 0.75rem 1.5rem;
  border: none;
  background: #EDF2F7;
  color: #4A5568;
  border-radius: 8px;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.2s ease;
}

.tab-button:hover {
  background: #E2E8F0;
}

.tab-button.active {
  background: #4299E1;
  color: white;
}

.comparison-cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
  margin-bottom: 3rem;
}

.comparison-card {
  padding: 2rem;
  border-radius: 12px;
  text-align: center;
  position: relative;
}

.comparison-card.traditional {
  background: #F7FAFC;
  border: 2px solid #E2E8F0;
}

.comparison-card.bioshuttle {
  background: #EBF8FF;
  border: 2px solid #4299E1;
}

.improvement-badge {
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
  background: #4299E1;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 500;
  white-space: nowrap;
}

.dosage-value {
  font-size: 2.5rem;
  font-weight: 700;
  color: #2D3748;
  margin: 1rem 0;
}

.dosage-label {
  color: #4A5568;
  margin-bottom: 1.5rem;
}

.feature-list {
  list-style: none;
  padding: 0;
  text-align: left;
}

.feature-list li {
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
  position: relative;
}

.feature-list li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

.key-metrics {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 2rem;
  padding-top: 2rem;
  border-top: 1px solid #E2E8F0;
}

.metric-box {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1.5rem;
  background: #F7FAFC;
  border-radius: 12px;
}

.metric-icon {
  width: 48px;
  height: 48px;
  background: #EBF8FF;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  color: #4299E1;
}

.metric-details {
  flex-grow: 1;
}

.metric-value {
  font-size: 1.5rem;
  font-weight: 700;
  color: #2D3748;
}

.metric-label {
  color: #4A5568;
  font-size: 0.875rem;
}

@media (max-width: 768px) {
  .comparison-cards {
    grid-template-columns: 1fr;
  }

  .key-metrics {
    grid-template-columns: 1fr;
  }

  .comparison-tabs {
    flex-direction: column;
  }

  .section-title {
    font-size: 2rem;
  }

  .comparison-container {
    padding: 1rem;
  }

  .improvement-badge {
    font-size: 0.75rem;
    padding: 0.25rem 0.75rem;
  }
}
</style>