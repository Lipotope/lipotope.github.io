// pages/Products.vue
<template>
  <Layout>
    <!-- Hero Section -->
    <ProductsHero />

    <!-- Main Content -->
    <div class="products-content">
      <div class="container">
        <!-- Current Products Section -->
        <section id="current-products" class="current-products">
          <CurrentProducts />
        </section>

        <!-- Pipeline Section -->
        <section id="pipeline" class="product-pipeline">
          <ProductPipeline />
        </section>

        <!-- Development Process Section -->
        <section id="development" class="development-process">
          <DevelopmentProcess />
        </section>

        <!-- CTA Section -->
        <section class="products-cta">
          <div class="cta-content">
            <h2>Ready to Transform Drug Delivery?</h2>
            <p>Discover distribution opportunities or explore custom formulations</p>
            <div class="cta-actions">
              <g-link to="/contact" class="btn btn-primary">
                Contact Us
              </g-link>
              <g-link to="/technology" class="btn btn-secondary">
                Learn More About Our Technology
              </g-link>
            </div>
          </div>

          <div class="key-stats">
            <div class="stat-item">
              <span class="stat-value">3</span>
              <span class="stat-label">Market-Ready Products</span>
            </div>
            <div class="stat-item">
              <span class="stat-value">4+</span>
              <span class="stat-label">Pipeline Products</span>
            </div>
            <div class="stat-item">
              <span class="stat-value">20x</span>
              <span class="stat-label">Faster Development</span>
            </div>
          </div>
        </section>
      </div>
    </div>
  </Layout>
</template>

<script>
import ProductsHero from '~/components/products/ProductsHero.vue'
import CurrentProducts from '~/components/products/CurrentProducts.vue'
import ProductPipeline from '~/components/products/ProductPipeline.vue'
import DevelopmentProcess from '~/components/products/DevelopmentProcess.vue'

export default {
  components: {
    ProductsHero,
    CurrentProducts,
    ProductPipeline,
    DevelopmentProcess
  },
  metaInfo: {
    title: 'Products - BioShuttle Drug Delivery Platform',
    meta: [
      { 
        name: 'description', 
        content: 'Discover BioShuttle\'s innovative product lineup and development pipeline.' 
      }
    ]
  }
}
</script>

<style scoped>
.products-content {
  padding: 4rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.current-products,
.product-pipeline,
.development-process {
  margin-bottom: 6rem;
  scroll-margin-top: 80px; /* For smooth scrolling with fixed header */
}

.products-cta {
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  border-radius: 16px;
  padding: 4rem;
  color: white;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.products-cta::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('/images/molecule-pattern.png') repeat;
  opacity: 0.1;
}

.cta-content {
  position: relative;
  z-index: 1;
  margin-bottom: 3rem;
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
  padding: 0.75rem 2rem;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.3s ease;
  text-decoration: none;
  display: inline-block;
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
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
}

.key-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  margin-top: 3rem;
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
  .current-products,
  .product-pipeline,
  .development-process {
    margin-bottom: 4rem;
  }

  .products-cta {
    padding: 3rem 2rem;
  }
}

@media (max-width: 768px) {
  .products-content {
    padding: 2rem 0;
  }

  .container {
    padding: 0 1rem;
  }

  .current-products,
  .product-pipeline,
  .development-process {
    margin-bottom: 3rem;
  }

  .products-cta {
    padding: 2rem 1.5rem;
  }

  .cta-content h2 {
    font-size: 2rem;
  }

  .cta-content p {
    font-size: 1.125rem;
  }

  .cta-actions {
    flex-direction: column;
  }

  .btn {
    width: 100%;
    text-align: center;
  }

  .key-stats {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .stat-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    justify-content: center;
  }

  .stat-value {
    margin-bottom: 0;
  }
}
</style>