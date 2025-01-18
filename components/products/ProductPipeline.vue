<template>
  <div class="pipeline-section">
    <div class="section-header">
      <h2 class="section-title">Development Pipeline</h2>
      <p class="section-subtitle">
        Innovative solutions in development leveraging BioShuttle technology
      </p>
    </div>

    <div class="pipeline-timeline">
      <!-- Development Stages Header -->
      <div class="timeline-header">
        <div class="stage-marker">
          <span>Research</span>
        </div>
        <div class="stage-marker">
          <span>Development</span>
        </div>
        <div class="stage-marker">
          <span>Testing</span>
        </div>
        <div class="stage-marker">
          <span>Final Stage</span>
        </div>
      </div>

      <!-- Pipeline Products -->
      <div class="pipeline-products">
        <!-- Athletic Performance Product -->
        <div class="pipeline-product">
          <div class="product-info">
            <div class="product-header">
              <h3>Athletic Performance</h3>
              <span class="category-tag">Sports Nutrition</span>
            </div>
            <p class="product-description">
              Performance enhancement and recovery optimization solution
            </p>
          </div>
          <div class="progress-track">
            <div class="progress-bar" style="width: 90%">
              <span class="progress-indicator"></span>
            </div>
          </div>
          <div class="timeline-info">
            <span class="expected-date">Q2 2025</span>
            <span class="status-tag final">Final Stage</span>
          </div>
        </div>

        <!-- Sleep & Anxiety Product -->
        <div class="pipeline-product">
          <div class="product-info">
            <div class="product-header">
              <h3>Sleep & Anxiety</h3>
              <span class="category-tag">Wellness</span>
            </div>
            <p class="product-description">
              Natural solution for anxiety-induced insomnia
            </p>
          </div>
          <div class="progress-track">
            <div class="progress-bar" style="width: 75%">
              <span class="progress-indicator"></span>
            </div>
          </div>
          <div class="timeline-info">
            <span class="expected-date">Q3 2025</span>
            <span class="status-tag testing">Testing</span>
          </div>
        </div>

        <!-- Neurological Product -->
        <div class="pipeline-product">
          <div class="product-info">
            <div class="product-header">
              <h3>Brain Health Formula</h3>
              <span class="category-tag">CNS</span>
            </div>
            <p class="product-description">
              Advanced cognitive support utilizing BBB penetration
            </p>
          </div>
          <div class="progress-track">
            <div class="progress-bar" style="width: 45%">
              <span class="progress-indicator"></span>
            </div>
          </div>
          <div class="timeline-info">
            <span class="expected-date">Q1 2026</span>
            <span class="status-tag development">Development</span>
          </div>
        </div>

        <!-- Research Stage Product -->
        <div class="pipeline-product">
          <div class="product-info">
            <div class="product-header">
              <h3>Immune Support</h3>
              <span class="category-tag">Wellness</span>
            </div>
            <p class="product-description">
              Enhanced immune system modulation formulation
            </p>
          </div>
          <div class="progress-track">
            <div class="progress-bar" style="width: 20%">
              <span class="progress-indicator"></span>
            </div>
          </div>
          <div class="timeline-info">
            <span class="expected-date">Q3 2026</span>
            <span class="status-tag research">Research</span>
          </div>
        </div>
      </div>
    </div>

    <div class="pipeline-legend">
      <div class="legend-item">
        <span class="status-tag research">Research</span>
        <span class="legend-text">Initial research and concept development</span>
      </div>
      <div class="legend-item">
        <span class="status-tag development">Development</span>
        <span class="legend-text">Active formulation development</span>
      </div>
      <div class="legend-item">
        <span class="status-tag testing">Testing</span>
        <span class="legend-text">Product testing and validation</span>
      </div>
      <div class="legend-item">
        <span class="status-tag final">Final Stage</span>
        <span class="legend-text">Preparing for market launch</span>
      </div>
    </div>
  </div>
</template>

<script setup>
// No dynamic logic required for this component
</script>

<style scoped>
.pipeline-section {
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

.pipeline-timeline {
  background: white;
  border-radius: 16px;
  padding: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin-bottom: 2rem;
}

.timeline-header {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  padding-bottom: 2rem;
  border-bottom: 2px solid #E2E8F0;
}

.stage-marker {
  text-align: center;
  color: #4A5568;
  font-weight: 500;
}

.pipeline-products {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  padding: 2rem 0;
}

.pipeline-product {
  display: grid;
  grid-template-columns: 1fr 2fr auto;
  gap: 2rem;
  align-items: center;
}

.product-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 0.5rem;
}

.product-header h3 {
  color: #2D3748;
  font-size: 1.25rem;
  margin: 0;
}

.category-tag {
  background: #EDF2F7;
  color: #4A5568;
  padding: 0.25rem 0.75rem;
  border-radius: 12px;
  font-size: 0.875rem;
}

.product-description {
  color: #718096;
  font-size: 0.875rem;
  margin: 0;
}

.progress-track {
  background: #EDF2F7;
  height: 8px;
  border-radius: 4px;
  position: relative;
}

.progress-bar {
  background: #4299E1;
  height: 100%;
  border-radius: 4px;
  position: relative;
}

.progress-indicator {
  width: 16px;
  height: 16px;
  background: #4299E1;
  border: 3px solid white;
  border-radius: 50%;
  position: absolute;
  right: -8px;
  top: 50%;
  transform: translateY(-50%);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.timeline-info {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 0.5rem;
}

.expected-date {
  color: #2D3748;
  font-weight: 500;
}

.status-tag {
  padding: 0.25rem 0.75rem;
  border-radius: 12px;
  font-size: 0.875rem;
  font-weight: 500;
}

.status-tag.research {
  background: #FC8181;
  color: white;
}

.status-tag.development {
  background: #F6E05E;
  color: #744210;
}

.status-tag.testing {
  background: #68D391;
  color: white;
}

.status-tag.final {
  background: #4299E1;
  color: white;
}

.pipeline-legend {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
  padding: 2rem;
  background: white;
  border-radius: 16px;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.legend-text {
  color: #4A5568;
  font-size: 0.875rem;
}

@media (max-width: 1024px) {
  .pipeline-product {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .timeline-info {
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .timeline-header {
    display: none;
  }

  .pipeline-legend {
    flex-direction: column;
    align-items: flex-start;
    gap: 1rem;
  }

  .pipeline-timeline {
    padding: 1rem;
  }
}
</style>