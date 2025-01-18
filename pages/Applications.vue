<template>
    <div>
      <!-- Hero Section -->
      <ApplicationsHero @application-selected="handleApplicationSelect" />
  
      <!-- Application Details Section -->
      <section v-if="selectedApplication" class="details-section">
        <ApplicationDetails :application="selectedApplication" />
      </section>
  
      <!-- Case Studies Section -->
      <section class="cases-section">
        <CaseStudies />
      </section>
  
      <!-- CTA Section -->
      <section class="applications-cta">
        <div class="container">
          <div class="cta-content">
            <h2>Transform Your Therapeutic Delivery</h2>
            <p>
              Discover how BioShuttle technology can enhance your therapeutic applications
            </p>
            <div class="cta-actions">
              <NuxtLink to="/contact" class="btn btn-primary">
                Contact Our Team
              </NuxtLink>
              <NuxtLink to="/technology" class="btn btn-secondary">
                Explore Our Technology
              </NuxtLink>
            </div>
          </div>
          <div class="stats-grid">
            <div class="stat-item">
              <span class="stat-value">50,000x</span>
              <span class="stat-label">Lower Dosing Requirements</span>
            </div>
            <div class="stat-item">
              <span class="stat-value">2 Years</span>
              <span class="stat-label">Room Temperature Stability</span>
            </div>
            <div class="stat-item">
              <span class="stat-value">20x</span>
              <span class="stat-label">Faster Development</span>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import ApplicationsHero from '~/components/applications/ApplicationsHero.vue'
  import ApplicationDetails from '~/components/applications/ApplicationDetails.vue'
  import CaseStudies from '~/components/applications/CaseStudies.vue'
  
  // Set page meta
  useHead({
    title: 'Applications - BioShuttle Drug Delivery Platform',
    meta: [
      {
        name: 'description',
        content: 'Explore BioShuttle\'s revolutionary applications in Gene Therapy, Cancer Treatment, Brain Drug Delivery, Vaccines, and Tissue Engineering.'
      }
    ]
  })
  
  // Reactive state for selected application
  const selectedApplication = ref(null)
  
  // Method to handle application selection
  const handleApplicationSelect = (application) => {
    selectedApplication.value = application
    
    // Use nextTick and scroll to details section
    nextTick(() => {
      const detailsSection = document.querySelector('.details-section')
      if (detailsSection) {
        detailsSection.scrollIntoView({ behavior: 'smooth', block: 'start' })
      }
    })
  }
  </script>
  
  <style scoped>
  .details-section {
    scroll-margin-top: 80px;
    background: #F7FAFC;
  }
  
  .cases-section {
    background: white;
  }
  
  .applications-cta {
    padding: 6rem 0;
    background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
    color: white;
    position: relative;
    overflow: hidden;
  }
  
  .applications-cta::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: url('/src/assets/images/molecule-pattern.png') repeat;
    opacity: 0.1;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }
  
  .cta-content {
    text-align: center;
    max-width: 800px;
    margin: 0 auto 4rem;
  }
  
  .cta-content h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }
  
  .cta-content p {
    font-size: 1.25rem;
    opacity: 0.9;
    margin-bottom: 2rem;
  }
  
  .cta-actions {
    display: flex;
    gap: 1rem;
    justify-content: center;
  }
  
  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.75rem 2rem;
    border-radius: 8px;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.3s ease;
  }
  
  .btn-primary {
    background: #4299E1;
    color: white;
  }
  
  .btn-primary:hover {
    background: #2B6CB0;
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
  
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 3rem;
    padding-top: 3rem;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
  }
  
  .stat-item {
    text-align: center;
  }
  
  .stat-value {
    display: block;
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  }
  
  .stat-label {
    font-size: 1rem;
    opacity: 0.9;
  }
  
  @media (max-width: 1024px) {
    .container {
      padding: 0 1.5rem;
    }
  
    .cta-content h2 {
      font-size: 2rem;
    }
  }
  
  @media (max-width: 768px) {
    .applications-cta {
      padding: 4rem 0;
    }
  
    .container {
      padding: 0 1rem;
    }
  
    .cta-content {
      margin-bottom: 2rem;
    }
  
    .cta-actions {
      flex-direction: column;
    }
  
    .btn {
      width: 100%;
    }
  
    .stats-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
  
    .stat-item {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  
    .stat-value {
      font-size: 2rem;
    }
  }
  
  @media (max-width: 480px) {
    .cta-content h2 {
      font-size: 1.75rem;
    }
  
    .cta-content p {
      font-size: 1.125rem;
    }
  }
  
  @media print {
    .applications-cta {
      background: white;
      color: #1A365D;
      padding: 2rem 0;
    }
  
    .btn {
      display: none;
    }
  
    .stats-grid {
      border-top-color: #E2E8F0;
    }
  }
  </style>