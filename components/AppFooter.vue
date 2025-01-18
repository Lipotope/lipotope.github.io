<template>
    <footer class="footer">
      <div class="footer-main">
        <div class="container">
          <div class="footer-grid">
            <!-- Company Info -->
            <div class="footer-column">
              <h4 class="footer-title">BioShuttle</h4>
              <p class="company-description">
                Revolutionary drug delivery platform utilizing proprietary stabilized liposomes
                to transform therapeutic compound delivery.
              </p>
            </div>
  
            <!-- Quick Links -->
            <div class="footer-column">
              <h4 class="footer-title">Quick Links</h4>
              <nav class="footer-nav">
                <NuxtLink to="/technology" class="footer-link">Technology</NuxtLink>
                <NuxtLink to="/applications" class="footer-link">Applications</NuxtLink>
                <NuxtLink to="/products" class="footer-link">Products</NuxtLink>
                <NuxtLink to="/about" class="footer-link">About Us</NuxtLink>
                <NuxtLink to="/contact" class="footer-link">Contact</NuxtLink>
              </nav>
            </div>
  
            <!-- Applications -->
            <div class="footer-column">
              <h4 class="footer-title">Applications</h4>
              <nav class="footer-nav">
                <NuxtLink to="/applications#gene-therapy" class="footer-link">Gene Therapy</NuxtLink>
                <NuxtLink to="/applications#cancer-therapy" class="footer-link">Cancer Therapy</NuxtLink>
                <NuxtLink to="/applications#brain-delivery" class="footer-link">Brain Drug Delivery</NuxtLink>
                <NuxtLink to="/applications#vaccines" class="footer-link">Vaccines</NuxtLink>
                <NuxtLink to="/applications#tissue-engineering" class="footer-link">Tissue Engineering</NuxtLink>
              </nav>
            </div>
  
            <!-- Contact Info -->
            <div class="footer-column">
              <h4 class="footer-title">Contact Us</h4>
              <div class="contact-info">
                <a href="mailto:info@bioshuttle.com" class="footer-link">
                  <span class="icon">✉</span> info@bioshuttle.com
                </a>
                <a href="tel:+1234567890" class="footer-link">
                  <span class="icon">📞</span> (123) 456-7890
                </a>
                <address class="address">
                  <span class="icon">📍</span> 123 Innovation Drive<br>
                  Suite 100<br>
                  Boston, MA 02110
                </address>
              </div>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Bottom Bar -->
      <div class="footer-bottom">
        <div class="container">
          <div class="footer-bottom-content">
            <p class="copyright">
              © {{ currentYear }} BioShuttle. All rights reserved.
            </p>
            <nav class="legal-nav">
              <NuxtLink to="/privacy" class="legal-link">Privacy Policy</NuxtLink>
              <NuxtLink to="/terms" class="legal-link">Terms of Service</NuxtLink>
            </nav>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script setup>
  const currentYear = computed(() => new Date().getFullYear())
  </script>
  
  <style scoped>
  .footer {
    background: #1a365d;
    color: white;
    margin-top: auto;
  }
  
  .footer-main {
    padding: 4rem 0;
  }
  
  .footer-grid {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr 1.5fr;
    gap: 3rem;
    padding: 0 2rem;
  }
  
  .footer-title {
    color: white;
    font-size: 1.25rem;
    margin-bottom: 1.5rem;
    font-weight: 600;
  }
  
  .company-description {
    color: #cbd5e0;
    line-height: 1.6;
  }
  
  .footer-nav {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
  }
  
  .footer-link {
    color: #cbd5e0;
    text-decoration: none;
    transition: color 0.2s ease;
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
  }
  
  .footer-link:hover {
    color: #4299e1;
  }
  
  .contact-info {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  
  .icon {
    display: inline-block;
    width: 1.5rem;
  }
  
  .address {
    color: #cbd5e0;
    font-style: normal;
    line-height: 1.6;
    margin-top: 0.5rem;
  }
  
  .footer-bottom {
    background: rgba(0, 0, 0, 0.2);
    padding: 1.5rem 1rem;
  }
  
  .footer-bottom-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .copyright {
    color: #cbd5e0;
    margin: 0;
  }
  
  .legal-nav {
    display: flex;
    gap: 2rem;
  }
  
  .legal-link {
    color: #cbd5e0;
    text-decoration: none;
    font-size: 0.875rem;
    transition: color 0.2s ease;
  }
  
  .legal-link:hover {
    color: #4299e1;
  }
  
  @media (max-width: 1024px) {
    .footer-grid {
      grid-template-columns: repeat(2, 1fr);
      gap: 2rem;
    }
  }
  
  @media (max-width: 640px) {
    .footer-grid {
      grid-template-columns: 1fr;
      gap: 2rem;
    }
  
    .footer-main {
      padding: 3rem 0;
    }
  
    .footer-bottom-content {
      flex-direction: column;
      gap: 1rem;
      text-align: center;
    }
  
    .legal-nav {
      justify-content: center;
    }
  }
  </style>