// components/applications/ApplicationsHero.vue
<template>
  <section class="applications-hero">
    <div class="container">
      <div class="hero-content">
        <h1>Therapeutic Applications</h1>
        <p class="lead">
          BioShuttle's versatile delivery platform enables breakthrough treatments 
          across multiple therapeutic areas
        </p>
      </div>

      <div class="applications-grid">
        <div v-for="(app, index) in applications" 
             :key="index"
             class="application-card"
             @click="selectApplication(app)">
          <div class="card-header">
            <div class="header-content">
              <h2>{{ app.title }}</h2>
              <span class="market-size">{{ app.marketSize }}</span>
            </div>
            <span class="growth-rate">{{ app.growth }} CAGR</span>
          </div>
          <p class="description">{{ app.description }}</p>
          <div class="key-points">
            <ul>
              <li v-for="(point, idx) in app.keyPoints" 
                  :key="idx">{{ point }}</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ApplicationsHero',
  data() {
    return {
      applications: [
        {
          title: 'Gene Therapy',
          marketSize: '$7.8B',
          growth: '27.8%',
          description: 'Safe delivery of DNA, RNA, and oligonucleotides directly to cell nucleus',
          keyPoints: [
            'Enhanced nuclear targeting',
            'Reduced cytotoxicity',
            'Cost-effective delivery'
          ]
        },
        {
          title: 'Cancer Therapy',
          marketSize: '$1.3B',
          growth: '5%',
          description: 'Development of highly targeted cytotoxic drugs with improved therapeutic indices',
          keyPoints: [
            'Targeted delivery',
            'Minimized side effects',
            'Enhanced efficacy'
          ]
        },
        {
          title: 'Brain Drug Delivery',
          marketSize: '$2.4B',
          growth: '32.1%',
          description: 'Non-invasive penetration of the blood-brain barrier',
          keyPoints: [
            'BBB penetration',
            'CNS targeting',
            'Reduced systemic exposure'
          ]
        },
        {
          title: 'Vaccines',
          marketSize: '$4.7B',
          growth: '10.5%',
          description: 'Advanced delivery system for antigens with sustained immune response',
          keyPoints: [
            'Needle-free delivery',
            'Enhanced stability',
            'Improved response'
          ]
        }
      ]
    }
  },
  methods: {
    selectApplication(application) {
      this.$emit('application-selected', application)
    }
  }
}
</script>

<style scoped>
.applications-hero {
  padding: 6rem 0;
  background: linear-gradient(135deg, #1a365d 0%, #2c5282 100%);
  color: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.hero-content {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 4rem;
}

.hero-content h1 {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.lead {
  font-size: 1.25rem;
  line-height: 1.6;
  opacity: 0.9;
}

.applications-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.application-card {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 2rem;
  cursor: pointer;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.application-card:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-5px);
}

.card-header {
  margin-bottom: 1.5rem;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.5rem;
}

.card-header h2 {
  font-size: 1.5rem;
  margin: 0;
}

.market-size {
  background: rgba(66, 153, 225, 0.3);
  padding: 0.25rem 0.75rem;
  border-radius: 20px;
  font-size: 0.875rem;
}

.growth-rate {
  font-size: 0.875rem;
  opacity: 0.8;
}

.description {
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  opacity: 0.9;
}

.key-points ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.key-points li {
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
  font-size: 0.875rem;
  opacity: 0.8;
}

.key-points li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

@media (max-width: 1024px) {
  .applications-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .applications-hero {
    padding: 4rem 0;
  }

  .hero-content h1 {
    font-size: 2rem;
  }

  .container {
    padding: 0 1rem;
  }

  .application-card {
    padding: 1.5rem;
  }
}
</style>