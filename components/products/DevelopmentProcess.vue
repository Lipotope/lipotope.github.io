<template>
  <div class="development-section">
    <div class="section-header">
      <h2 class="section-title">Development Process</h2>
      <p class="section-subtitle">
        Our streamlined approach accelerates development while maintaining the highest standards
      </p>
    </div>

    <div class="process-container">
      <!-- Process Timeline -->
      <div class="process-timeline">
        <!-- Research & Analysis -->
        <div class="process-step">
          <div class="step-number">01</div>
          <div class="step-content">
            <h3>Research & Analysis</h3>
            <p class="step-description">
              Comprehensive analysis of therapeutic compounds and delivery requirements
            </p>
            <div class="step-details">
              <h4>Key Activities</h4>
              <ul>
                <li>Compound analysis</li>
                <li>Delivery requirements assessment</li>
                <li>Market opportunity evaluation</li>
                <li>Initial feasibility studies</li>
              </ul>
              <div class="timeline-marker">
                <span class="duration">2-4 Weeks</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Formulation Development -->
        <div class="process-step">
          <div class="step-number">02</div>
          <div class="step-content">
            <h3>Formulation Development</h3>
            <p class="step-description">
              Rapid prototyping using proprietary BioShuttle technology
            </p>
            <div class="step-details">
              <h4>Key Activities</h4>
              <ul>
                <li>Prototype formulation</li>
                <li>Stability testing</li>
                <li>Bioavailability optimization</li>
                <li>Process refinement</li>
              </ul>
              <div class="timeline-marker">
                <span class="duration">4-6 Weeks</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Testing & Validation -->
        <div class="process-step">
          <div class="step-number">03</div>
          <div class="step-content">
            <h3>Testing & Validation</h3>
            <p class="step-description">
              Comprehensive testing to ensure safety and efficacy
            </p>
            <div class="step-details">
              <h4>Key Activities</h4>
              <ul>
                <li>Safety assessment</li>
                <li>Efficacy validation</li>
                <li>Stability confirmation</li>
                <li>Performance testing</li>
              </ul>
              <div class="timeline-marker">
                <span class="duration">6-8 Weeks</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Scale-Up & Manufacturing -->
        <div class="process-step">
          <div class="step-number">04</div>
          <div class="step-content">
            <h3>Scale-Up & Manufacturing</h3>
            <p class="step-description">
              Efficient scale-up process for commercial production
            </p>
            <div class="step-details">
              <h4>Key Activities</h4>
              <ul>
                <li>Process scale-up</li>
                <li>Quality control implementation</li>
                <li>Manufacturing optimization</li>
                <li>Production validation</li>
              </ul>
              <div class="timeline-marker">
                <span class="duration">4-6 Weeks</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Development Highlights -->
      <div class="development-highlights">
        <div class="highlight-card">
          <div class="highlight-icon">⚡</div>
          <div class="highlight-content">
            <h4>Accelerated Development</h4>
            <p>20x faster formulation development compared to traditional methods</p>
          </div>
        </div>

        <div class="highlight-card">
          <div class="highlight-icon">🎯</div>
          <div class="highlight-content">
            <h4>Proven Process</h4>
            <p>Successfully applied across multiple therapeutic areas</p>
          </div>
        </div>

        <div class="highlight-card">
          <div class="highlight-icon">📈</div>
          <div class="highlight-content">
            <h4>Efficient Scale-Up</h4>
            <p>Streamlined transition from development to commercial production</p>
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
.development-section {
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

.process-container {
  background: white;
  border-radius: 16px;
  padding: 3rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.process-timeline {
  position: relative;
  padding-left: 2rem;
}

.process-timeline::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  width: 2px;
  background: #E2E8F0;
}

.process-step {
  position: relative;
  padding-bottom: 3rem;
}

.process-step:last-child {
  padding-bottom: 0;
}

.step-number {
  position: absolute;
  left: -2.5rem;
  top: 0;
  width: 36px;
  height: 36px;
  background: #4299E1;
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  z-index: 1;
}

.step-content {
  padding-left: 2rem;
}

.step-content h3 {
  color: #2D3748;
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.step-description {
  color: #4A5568;
  font-size: 1.125rem;
  margin-bottom: 1.5rem;
}

.step-details h4 {
  color: #2D3748;
  font-size: 1.125rem;
  margin-bottom: 1rem;
}

.step-details ul {
  list-style: none;
  padding: 0;
  margin-bottom: 1rem;
}

.step-details li {
  color: #4A5568;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
}

.step-details li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

.timeline-marker {
  display: inline-block;
  background: #EBF8FF;
  padding: 0.5rem 1rem;
  border-radius: 20px;
}

.duration {
  color: #4299E1;
  font-weight: 500;
  font-size: 0.875rem;
}

.development-highlights {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 4rem;
  padding-top: 3rem;
  border-top: 2px solid #E2E8F0;
}

.highlight-card {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.highlight-icon {
  width: 48px;
  height: 48px;
  background: #EBF8FF;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
}

.highlight-content h4 {
  color: #2D3748;
  font-size: 1.125rem;
  margin-bottom: 0.5rem;
}

.highlight-content p {
  color: #4A5568;
  font-size: 0.875rem;
  line-height: 1.6;
}

@media (max-width: 1024px) {
  .development-highlights {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }

  .process-container {
    padding: 1.5rem;
  }

  .process-timeline {
    padding-left: 1rem;
  }

  .step-content {
    padding-left: 1rem;
  }

  .development-highlights {
    grid-template-columns: 1fr;
  }

  .step-number {
    left: -1.5rem;
    width: 30px;
    height: 30px;
    font-size: 0.875rem;
  }
}
</style>