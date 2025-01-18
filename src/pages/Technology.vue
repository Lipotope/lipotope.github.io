// pages/Technology.vue
<template>
  <Layout>
    <!-- Main technology overview section -->
    <TechnologyOverview />
    
    <!-- Benefits Grid section -->
    <section class="platform-benefits">
      <div class="container">
        <BenefitsGrid />
      </div>
    </section>

    <!-- Bioavailability Comparison section -->
    <section class="bioavailability">
      <div class="container">
        <BioavailabilityComparison />
      </div>
    </section>

    <!-- Platform Features section -->
    <section class="features">
      <div class="container">
        <PlatformFeatures />
      </div>
    </section>
  </Layout>
</template>

<script>
import TechnologyOverview from '~/components/technology/TechnologyOverview.vue'
import BenefitsGrid from '~/components/technology/BenefitsGrid.vue'
import BioavailabilityComparison from '~/components/technology/BioavailabilityComparison.vue'
import PlatformFeatures from '~/components/technology/PlatformFeatures.vue'

export default {
  components: {
    TechnologyOverview,
    BenefitsGrid,
    BioavailabilityComparison,
    PlatformFeatures
  },
  metaInfo: {
    title: 'BioShuttle Technology - Revolutionary Drug Delivery Platform'
  }
}
</script>

<style scoped>
.platform-benefits {
  padding: 6rem 0;
  background: white;
}

.bioavailability {
  padding: 6rem 0;
  background: #F8FAFC;
}

.features {
  padding: 6rem 0;
  background: white;
}

@media (max-width: 768px) {
  .platform-benefits,
  .bioavailability,
  .features {
    padding: 4rem 0;
  }
}
</style>