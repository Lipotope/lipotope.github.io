// components/technology/BenefitsGrid.vue
<template>
  <div class="benefits-section">
    <div class="section-header">
      <h2 class="section-title">Transformative Benefits</h2>
      <p class="section-subtitle">
        BioShuttle's revolutionary technology offers unprecedented advantages in drug delivery
      </p>
    </div>

    <div class="benefits-grid">
      <!-- Enhanced Bioavailability -->
      <div class="benefit-card" @mouseenter="hover = 1" @mouseleave="hover = null"
           :class="{ 'is-hovered': hover === 1 }">
        <div class="benefit-icon">
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path d="M13 2L3 14H12L11 22L21 10H12L13 2Z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <h3 class="benefit-title">Enhanced Bioavailability</h3>
        <p class="benefit-description">
          Achieve optimal therapeutic effects with doses up to 50,000-fold lower than traditional delivery methods
        </p>
        <ul class="benefit-points">
          <li>Dramatically reduced API requirements</li>
          <li>Lower production costs</li>
          <li>Minimized side effects</li>
        </ul>
      </div>

      <!-- Blood-Brain Barrier -->
      <div class="benefit-card" @mouseenter="hover = 2" @mouseleave="hover = null"
           :class="{ 'is-hovered': hover === 2 }">
        <div class="benefit-icon">
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <circle cx="12" cy="12" r="10" stroke-width="2"/>
            <path d="M8 12H16M12 8V16" stroke-width="2" stroke-linecap="round"/>
          </svg>
        </div>
        <h3 class="benefit-title">Blood-Brain Barrier Penetration</h3>
        <p class="benefit-description">
          Revolutionary ability to deliver therapeutic compounds directly to the brain
        </p>
        <ul class="benefit-points">
          <li>Non-invasive delivery method</li>
          <li>Targeted brain treatment</li>
          <li>Enhanced neurological outcomes</li>
        </ul>
      </div>

      <!-- Exceptional Stability -->
      <div class="benefit-card" @mouseenter="hover = 3" @mouseleave="hover = null"
           :class="{ 'is-hovered': hover === 3 }">
        <div class="benefit-icon">
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path d="M12 8V12L15 15" stroke-width="2" stroke-linecap="round"/>
            <circle cx="12" cy="12" r="10" stroke-width="2"/>
          </svg>
        </div>
        <h3 class="benefit-title">Exceptional Stability</h3>
        <p class="benefit-description">
          Unprecedented two-year shelf life at room temperature
        </p>
        <ul class="benefit-points">
          <li>Room temperature storage</li>
          <li>Extended shelf life</li>
          <li>Reduced logistics costs</li>
        </ul>
      </div>

      <!-- Cost Efficiency -->
      <div class="benefit-card" @mouseenter="hover = 4" @mouseleave="hover = null"
           :class="{ 'is-hovered': hover === 4 }">
        <div class="benefit-icon">
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path d="M12 1V23" stroke-width="2" stroke-linecap="round"/>
            <path d="M17 5H9.5C8.57174 5 7.6815 5.36875 7.02513 6.02513C6.36875 6.6815 6 7.57174 6 8.5C6 9.42826 6.36875 10.3185 7.02513 10.9749C7.6815 11.6313 8.57174 12 9.5 12H14.5C15.4283 12 16.3185 12.3687 16.9749 13.0251C17.6313 13.6815 18 14.5717 18 15.5C18 16.4283 17.6313 17.3185 16.9749 17.9749C16.3185 18.6313 15.4283 19 14.5 19H6" stroke-width="2" stroke-linecap="round"/>
          </svg>
        </div>
        <h3 class="benefit-title">Cost Efficiency</h3>
        <p class="benefit-description">
          Minimal added cost per dose compared to traditional delivery methods
        </p>
        <ul class="benefit-points">
          <li>Reduced API usage</li>
          <li>Simplified manufacturing</li>
          <li>Lower storage costs</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BenefitsGrid',
  data() {
    return {
      hover: null
    }
  }
}
</script>

<style scoped>
.benefits-section {
  padding: 2rem 0;
}

.section-header {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 4rem;
}

.section-title {
  color: #1a365d;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.section-subtitle {
  color: #4a5568;
  font-size: 1.25rem;
  line-height: 1.6;
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.benefit-card {
  background: white;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.benefit-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: linear-gradient(90deg, #4299e1, #2b6cb0);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.3s ease;
}

.benefit-card.is-hovered {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
}

.benefit-card.is-hovered::before {
  transform: scaleX(1);
}

.benefit-icon {
  width: 48px;
  height: 48px;
  background: #ebf8ff;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.5rem;
  color: #4299e1;
}

.icon {
  width: 24px;
  height: 24px;
}

.benefit-title {
  color: #2d3748;
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.benefit-description {
  color: #4a5568;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.benefit-points {
  list-style: none;
  padding: 0;
  margin: 0;
}

.benefit-points li {
  color: #718096;
  margin-bottom: 0.5rem;
  padding-left: 1.5rem;
  position: relative;
}

.benefit-points li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: #4299e1;
}

@media (max-width: 1024px) {
  .benefits-grid {
    gap: 1.5rem;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .benefit-title {
    font-size: 1.25rem;
  }
}

@media (max-width: 768px) {
  .benefits-grid {
    grid-template-columns: 1fr;
  }
  
  .benefits-section {
    padding: 1rem 0;
  }
  
  .section-header {
    margin-bottom: 2rem;
  }
}
</style>