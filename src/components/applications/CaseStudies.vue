// components/applications/CaseStudies.vue
<template>
  <section class="case-studies">
    <div class="container">
      <div class="section-header">
        <h2>Proof of Concept</h2>
        <p class="section-subtitle">
          Five groundbreaking proof-of-concept treatments demonstrating BioShuttle's versatility
        </p>
      </div>

      <!-- Featured UK Market Success -->
      <div class="featured-case">
        <div class="featured-content">
          <div class="status">
            <span class="status-badge success">Market Success</span>
            <span class="market-badge">UK Market</span>
          </div>
          <h3>Weight Management Solution</h3>
          <p class="featured-description">
            Successful diet formulation launched in the United Kingdom with exponentially growing sales
          </p>
          <div class="metrics">
            <div class="metric">
              <span class="metric-label">Time in Market</span>
              <span class="metric-value">4+ Months</span>
            </div>
            <div class="metric">
              <span class="metric-label">Sales Growth</span>
              <span class="metric-value">Exponential</span>
            </div>
            <div class="metric">
              <span class="metric-label">Market Reception</span>
              <span class="metric-value">Positive</span>
            </div>
          </div>
          <div class="highlights">
            <h4>Key Achievements</h4>
            <ul>
              <li>Successful market penetration</li>
              <li>Strong consumer adoption</li>
              <li>Validated efficacy profile</li>
              <li>Expanding distribution network</li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Recent Launches Grid -->
      <div class="recent-launches">
        <h3>Recent Product Launches</h3>
        <div class="launches-grid">
          <!-- Pain Relief -->
          <div class="case-card">
            <div class="card-header">
              <span class="status-badge new">New Launch</span>
              <span class="market-badge">US Market</span>
            </div>
            <div class="card-content">
              <h4>Pain Relief Innovation</h4>
              <p class="description">
                Novel pain management solution utilizing targeted delivery for enhanced efficacy
              </p>
              <div class="case-details">
                <div class="detail-row">
                  <span class="detail-label">Category</span>
                  <span class="detail-value">OTC</span>
                </div>
                <div class="detail-row">
                  <span class="detail-label">Launch Date</span>
                  <span class="detail-value">Q4 2024</span>
                </div>
                <div class="detail-row">
                  <span class="detail-label">Status</span>
                  <span class="detail-value">Active</span>
                </div>
              </div>
              <div class="key-features">
                <ul>
                  <li>Rapid onset of action</li>
                  <li>Extended duration</li>
                  <li>Minimal side effects</li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Intimacy Product -->
          <div class="case-card">
            <div class="card-header">
              <span class="status-badge new">New Launch</span>
              <span class="market-badge">US Market</span>
            </div>
            <div class="card-content">
              <h4>Postmenopausal Wellness</h4>
              <p class="description">
                Innovative intimacy solution addressing postmenopausal concerns with targeted delivery
              </p>
              <div class="case-details">
                <div class="detail-row">
                  <span class="detail-label">Category</span>
                  <span class="detail-value">Wellness</span>
                </div>
                <div class="detail-row">
                  <span class="detail-label">Launch Date</span>
                  <span class="detail-value">Q4 2024</span>
                </div>
                <div class="detail-row">
                  <span class="detail-label">Status</span>
                  <span class="detail-value">Active</span>
                </div>
              </div>
              <div class="key-features">
                <ul>
                  <li>Enhanced absorption</li>
                  <li>Targeted action</li>
                  <li>Gentle formulation</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Development Pipeline -->
      <div class="development-pipeline">
        <h3>Advanced Development Stage</h3>
        <div class="pipeline-grid">
          <!-- Athletic Performance -->
          <div class="pipeline-card">
            <div class="card-header">
              <span class="status-badge pipeline">Final Stage</span>
            </div>
            <div class="card-content">
              <h4>Athletic Performance</h4>
              <p class="description">
                Performance enhancement and recovery optimization through targeted nutrient delivery
              </p>
              <div class="timeline">
                <span class="timeline-label">Expected Launch</span>
                <span class="timeline-value">Q2 2025</span>
              </div>
              <div class="development-status">
                <div class="status-bar">
                  <div class="status-progress" style="width: 90%"></div>
                </div>
                <span class="status-text">90% Complete</span>
              </div>
            </div>
          </div>

          <!-- Sleep & Anxiety -->
          <div class="pipeline-card">
            <div class="card-header">
              <span class="status-badge pipeline">Testing</span>
            </div>
            <div class="card-content">
              <h4>Sleep & Anxiety</h4>
              <p class="description">
                Innovative solution for anxiety-induced insomnia with improved bioavailability
              </p>
              <div class="timeline">
                <span class="timeline-label">Expected Launch</span>
                <span class="timeline-value">Q3 2025</span>
              </div>
              <div class="development-status">
                <div class="status-bar">
                  <div class="status-progress" style="width: 75%"></div>
                </div>
                <span class="status-text">75% Complete</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CaseStudies'
}
</script>

<style scoped>
.case-studies {
  padding: 4rem 0;
  background: #F7FAFC;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-header {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 4rem;
}

.section-header h2 {
  color: #1A365D;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.section-subtitle {
  color: #4A5568;
  font-size: 1.25rem;
  line-height: 1.6;
}

/* Featured Case Study */
.featured-case {
  background: white;
  border-radius: 16px;
  padding: 2.5rem;
  margin-bottom: 4rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.featured-case:hover {
  transform: translateY(-5px);
}

.featured-content {
  max-width: 800px;
}

.status {
  display: flex;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.status-badge {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.875rem;
  font-weight: 500;
  transition: all 0.3s ease;
}

.status-badge.success {
  background: #48BB78;
  color: white;
}

.status-badge.new {
  background: #4299E1;
  color: white;
}

.status-badge.pipeline {
  background: #ED8936;
  color: white;
}

.market-badge {
  padding: 0.5rem 1rem;
  border-radius: 20px;
  background: #EDF2F7;
  color: #2D3748;
  font-size: 0.875rem;
  font-weight: 500;
}

.featured-case h3 {
  color: #2D3748;
  font-size: 1.875rem;
  margin-bottom: 1rem;
}

.featured-description {
  color: #4A5568;
  font-size: 1.25rem;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.metrics {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-bottom: 2rem;
  padding: 2rem 0;
  border-top: 1px solid #E2E8F0;
  border-bottom: 1px solid #E2E8F0;
}

.metric {
  text-align: center;
}

.metric-label {
  display: block;
  color: #718096;
  font-size: 0.875rem;
  margin-bottom: 0.5rem;
}

.metric-value {
  color: #2D3748;
  font-size: 1.5rem;
  font-weight: 600;
}

.highlights h4 {
  color: #2D3748;
  font-size: 1.25rem;
  margin-bottom: 1rem;
}

.highlights ul {
  list-style: none;
  padding: 0;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1rem;
}

.highlights li {
  color: #4A5568;
  padding-left: 1.5rem;
  position: relative;
  line-height: 1.6;
}

.highlights li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

/* Recent Launches */
.recent-launches {
  margin-bottom: 4rem;
}

.recent-launches h3 {
  color: #2D3748;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}

.launches-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.case-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.case-card:hover {
  transform: translateY(-5px);
}

.card-header {
  padding: 1.5rem;
  background: #F7FAFC;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.card-content {
  padding: 1.5rem;
}

.card-content h4 {
  color: #2D3748;
  font-size: 1.25rem;
  margin-bottom: 1rem;
}

.description {
  color: #4A5568;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.case-details {
  margin-bottom: 1.5rem;
}

.detail-row {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 0;
  border-bottom: 1px solid #E2E8F0;
}

.detail-row:last-child {
  border-bottom: none;
}

.detail-label {
  color: #718096;
  font-size: 0.875rem;
}

.detail-value {
  color: #2D3748;
  font-weight: 500;
}

.key-features ul {
  list-style: none;
  padding: 0;
}

.key-features li {
  color: #4A5568;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
  line-height: 1.6;
}

.key-features li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

/* Development Pipeline */
.development-pipeline {
  margin-bottom: 2rem;
}

.development-pipeline h3 {
  color: #2D3748;
  font-size: 1.5rem;
  margin-bottom: 2rem;
}

.pipeline-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.pipeline-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.pipeline-card:hover {
  transform: translateY(-5px);
}

.timeline {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1.5rem;
}

.timeline-label {
  color: #718096;
  font-size: 0.875rem;
}

.timeline-value {
  color: #2D3748;
  font-weight: 500;
}

.development-status {
  margin-top: 1rem;
}

.status-bar {
  height: 8px;
  background: #EDF2F7;
  border-radius: 4px;
  overflow: hidden;
  margin-bottom: 0.5rem;
}

.status-progress {
  height: 100%;
  background: #4299E1;
  border-radius: 4px;
  transition: width 0.3s ease;
}

.status-text {
  color: #718096;
  font-size: 0.875rem;
}

/* Hover States */
.status-badge:hover {
  transform: translateY(-1px);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card-header .status-badge:hover {
  opacity: 0.9;
}

/* Animations */
@keyframes progressFill {
  from {
    width: 0;
  }
  to {
    width: 100%;
  }
}

.status-progress {
  animation: progressFill 1s ease-out;
}

/* Responsive Design */
@media (max-width: 1024px) {
  .container {
    padding: 0 1.5rem;
  }

  .metrics,
  .highlights ul {
    grid-template-columns: repeat(2, 1fr);
  }

  .launches-grid,
  .pipeline-grid {
    gap: 1.5rem;
  }
}

@media (max-width: 768px) {
  .case-studies {
    padding: 2rem 0;
  }

  .container {
    padding: 0 1rem;
  }

  .section-header h2 {
    font-size: 2rem;
  }

  .section-subtitle {
    font-size: 1.125rem;
  }

  .featured-case {
    padding: 1.5rem;
  }

  .featured-case h3 {
    font-size: 1.5rem;
  }

  .featured-description {
    font-size: 1.125rem;
  }

  .launches-grid,
  .pipeline-grid {
    grid-template-columns: 1fr;
  }

  .metrics {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .highlights ul {
    grid-template-columns: 1fr;
  }

  .metric {
    text-align: left;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .metric-label {
    margin-bottom: 0;
  }

  .card-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
}

@media (max-width: 480px) {
  .section-header {
    margin-bottom: 2rem;
  }

  .featured-case {
    padding: 1rem;
  }

  .status {
    flex-direction: column;
    gap: 0.5rem;
  }

  .card-content {
    padding: 1rem;
  }

  .detail-row {
    flex-direction: column;
    gap: 0.25rem;
  }

  .detail-value {
    padding-left: 1rem;
  }

  .timeline {
    flex-direction: column;
    align-items: flex-start;
    gap: 0.5rem;
  }
}

/* Print Styles */
@media print {
  .case-studies {
    padding: 0;
  }

  .case-card,
  .pipeline-card,
  .featured-case {
    break-inside: avoid;
    box-shadow: none;
  }

  .status-progress {
    print-color-adjust: exact;
    -webkit-print-color-adjust: exact;
  }
}
</style>