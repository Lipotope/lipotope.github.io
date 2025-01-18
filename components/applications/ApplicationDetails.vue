<template>
  <section v-if="application" class="application-details">
    <div class="container">
      <div class="details-card">
        <div class="card-header">
          <div class="header-content">
            <h2>{{ application.title }}</h2>
            <div class="market-stats">
              <div class="stat">
                <span class="stat-label">Market Size</span>
                <span class="stat-value">{{ application.marketSize }}</span>
              </div>
              <div class="stat">
                <span class="stat-label">Growth Rate</span>
                <span class="stat-value">{{ application.growth }}</span>
              </div>
            </div>
          </div>
        </div>

        <div class="card-body">
          <!-- Technical Overview -->
          <div class="section">
            <h3>Technical Overview</h3>
            <p class="technical-description">{{ technicalDescription }}</p>
            <div class="technical-highlights">
              <div class="highlight-item" v-for="(highlight, index) in technicalHighlightsList" 
                   :key="index">
                <div class="highlight-icon">{{ highlight.icon }}</div>
                <div class="highlight-content">
                  <h4>{{ highlight.title }}</h4>
                  <p>{{ highlight.description }}</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Implementation Details -->
          <div class="section">
            <h3>Implementation</h3>
            <div class="implementation-grid">
              <div class="implementation-item" v-for="(detail, index) in implementationDetailsList" 
                   :key="index">
                <h4>{{ detail.phase }}</h4>
                <ul>
                  <li v-for="(step, stepIndex) in detail.steps" 
                      :key="stepIndex">{{ step }}</li>
                </ul>
              </div>
            </div>
          </div>

          <!-- Performance Metrics -->
          <div class="section">
            <h3>Performance Metrics</h3>
            <div class="metrics-grid">
              <div class="metric-card" v-for="(metric, index) in performanceMetricsList" 
                   :key="index">
                <span class="metric-value">{{ metric.value }}</span>
                <span class="metric-label">{{ metric.label }}</span>
                <span class="metric-description">{{ metric.description }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps({
  application: {
    type: Object,
    required: true
  }
})

const technicalDescriptions = {
  'Gene Therapy': 'BioShuttle enables precise delivery of genetic material including DNA, RNA, siRNA, oligonucleotides, and plasmids directly to the cell nucleus, achieving enhanced transfection efficiency while maintaining cell viability. This provides an alternative to costly transfection agents with improved targeting and reduced cytotoxicity.',
  'Cancer Therapy': 'Our targeted delivery system optimizes therapeutic payload distribution for highly cytotoxic drugs, maximizing efficacy at tumor sites while minimizing systemic exposure. This dramatically improves the therapeutic index and reduces side effects commonly associated with cancer treatments.',
  'Brain Drug Delivery': 'Non-invasive blood-brain barrier penetration enables direct CNS therapeutic delivery through BioShuttle\'s revolutionary delivery mechanism. This breakthrough allows for the treatment of previously inaccessible neurological conditions with validated penetration pathways.',
  'Vaccines': 'Advanced antigen delivery platform enables sustained immune response through optimized presentation and controlled release mechanisms. This needle-free administration system improves stability and provides enhanced immunological responses without traditional delivery constraints.',
  'Tissue Engineering': 'Targeted delivery of growth and differentiation factors enables precise tissue regeneration with controlled release profiles. This innovative approach enhances tissue integration and improves regenerative outcomes across multiple applications.'
}

const technicalHighlights = {
  'Gene Therapy': [
    {
      icon: '🎯',
      title: 'Nuclear Targeting',
      description: 'Enhanced nuclear localization for direct delivery'
    },
    {
      icon: '🔬',
      title: 'Cellular Uptake',
      description: 'Optimized particle design for maximum penetration'
    },
    {
      icon: '⚡',
      title: 'Expression Efficiency',
      description: 'Sustained therapeutic expression profiles'
    }
  ],
  'Cancer Therapy': [
    {
      icon: '🎯',
      title: 'Tumor Targeting',
      description: 'Precise delivery to tumor sites'
    },
    {
      icon: '⚡',
      title: 'Enhanced Efficacy',
      description: 'Improved therapeutic index'
    },
    {
      icon: '🛡️',
      title: 'Reduced Toxicity',
      description: 'Minimized systemic exposure'
    }
  ],
  'Brain Drug Delivery': [
    {
      icon: '🧠',
      title: 'BBB Penetration',
      description: 'Effective barrier crossing'
    },
    {
      icon: '🎯',
      title: 'CNS Targeting',
      description: 'Precise neurological delivery'
    },
    {
      icon: '⚡',
      title: 'Rapid Distribution',
      description: 'Optimized brain tissue coverage'
    }
  ],
  'Vaccines': [
    {
      icon: '🛡️',
      title: 'Enhanced Response',
      description: 'Improved immune activation'
    },
    {
      icon: '⚡',
      title: 'Stability',
      description: 'Extended shelf life at room temperature'
    },
    {
      icon: '💉',
      title: 'Needle-Free',
      description: 'Non-invasive administration'
    }
  ],
  'Tissue Engineering': [
    {
      icon: '🎯',
      title: 'Targeted Release',
      description: 'Controlled factor delivery'
    },
    {
      icon: '🔄',
      title: 'Integration',
      description: 'Enhanced tissue development'
    },
    {
      icon: '⚡',
      title: 'Regeneration',
      description: 'Optimized healing response'
    }
  ]
}

const implementationDetails = {
  'Gene Therapy': [
    {
      phase: 'Formulation',
      steps: [
        'Particle size optimization',
        'Surface modification',
        'Stability enhancement',
        'Nucleic acid protection'
      ]
    },
    {
      phase: 'Delivery',
      steps: [
        'Nuclear targeting integration',
        'Controlled release mechanism',
        'Cellular uptake optimization',
        'Expression efficiency'
      ]
    },
    {
      phase: 'Validation',
      steps: [
        'Expression analysis',
        'Viability assessment',
        'Long-term stability',
        'Safety verification'
      ]
    }
  ],
  'Cancer Therapy': [
    {
      phase: 'Targeting',
      steps: [
        'Tumor-specific binding',
        'Enhanced permeability',
        'Retention optimization',
        'Distribution analysis'
      ]
    },
    {
      phase: 'Delivery',
      steps: [
        'Controlled drug release',
        'Local concentration',
        'Systemic exposure control',
        'Bioavailability enhancement'
      ]
    },
    {
      phase: 'Validation',
      steps: [
        'Therapeutic index',
        'Safety profiling',
        'Efficacy confirmation',
        'Clinical assessment'
      ]
    }
  ],
  'Brain Drug Delivery': [
    {
      phase: 'BBB Strategy',
      steps: [
        'Barrier penetration',
        'Transport enhancement',
        'Distribution optimization',
        'CNS targeting'
      ]
    },
    {
      phase: 'Delivery',
      steps: [
        'Non-invasive administration',
        'Rapid distribution',
        'Sustained presence',
        'Controlled release'
      ]
    },
    {
      phase: 'Validation',
      steps: [
        'CNS penetration',
        'Distribution mapping',
        'Safety assessment',
        'Efficacy verification'
      ]
    }
  ],
  'Vaccines': [
    {
      phase: 'Antigen Design',
      steps: [
        'Stability optimization',
        'Immune recognition',
        'Release profiling',
        'Adjuvant integration'
      ]
    },
    {
      phase: 'Delivery',
      steps: [
        'Non-invasive administration',
        'Controlled release',
        'Tissue targeting',
        'Immune cell activation'
      ]
    },
    {
      phase: 'Validation',
      steps: [
        'Immune response',
        'Duration assessment',
        'Safety profiling',
        'Stability confirmation'
      ]
    }
  ],
  'Tissue Engineering': [
    {
      phase: 'Factor Design',
      steps: [
        'Growth factor selection',
        'Release optimization',
        'Stability enhancement',
        'Integration planning'
      ]
    },
    {
      phase: 'Delivery',
      steps: [
        'Targeted release',
        'Spatial control',
        'Temporal regulation',
        'Local concentration'
      ]
    },
    {
      phase: 'Validation',
      steps: [
        'Tissue development',
        'Integration assessment',
        'Function verification',
        'Long-term stability'
      ]
    }
  ]
}

const performanceMetrics = {
  'Gene Therapy': [
    {
      value: '95%+',
      label: 'Delivery Efficiency',
      description: 'Nuclear localization success rate'
    },
    {
      value: '80%',
      label: 'Cost Reduction',
      description: 'Compared to traditional methods'
    },
    {
      value: '3x',
      label: 'Expression Duration',
      description: 'Extended therapeutic window'
    }
  ],
  'Cancer Therapy': [
    {
      value: '90%+',
      label: 'Target Specificity',
      description: 'Tumor site accumulation'
    },
    {
      value: '75%',
      label: 'Side Effect Reduction',
      description: 'Decreased systemic toxicity'
    },
    {
      value: '4x',
      label: 'Therapeutic Index',
      description: 'Improved safety margin'
    }
  ],
  'Brain Drug Delivery': [
    {
      value: '85%+',
      label: 'BBB Penetration',
      description: 'Successful barrier crossing'
    },
    {
      value: '70%',
      label: 'CNS Distribution',
      description: 'Brain tissue coverage'
    },
    {
      value: '5x',
      label: 'Bioavailability',
      description: 'Increased brain concentration'
    }
  ],
  'Vaccines': [
    {
      value: '2 Years',
      label: 'Stability',
      description: 'Room temperature storage'
    },
    {
      value: '3x',
      label: 'Immune Response',
      description: 'Enhanced activation'
    },
    {
      value: '100%',
      label: 'Needle-Free',
      description: 'Non-invasive administration'
    }
  ],
  'Tissue Engineering': [
    {
      value: '90%+',
      label: 'Factor Delivery',
      description: 'Targeted release efficiency'
    },
    {
      value: '4x',
      label: 'Integration',
      description: 'Improved tissue development'
    },
    {
      value: '2x',
      label: 'Recovery Time',
      description: 'Accelerated healing'
    }
  ]
}

// Computed properties to dynamically fetch data based on application title
const technicalDescription = computed(() => 
  technicalDescriptions[props.application.title] || ''
)

const technicalHighlightsList = computed(() => 
  technicalHighlights[props.application.title] || []
)

const implementationDetailsList = computed(() => 
  implementationDetails[props.application.title] || []
)

const performanceMetricsList = computed(() => 
  performanceMetrics[props.application.title] || []
)
</script>

<style scoped>
.application-details {
  padding: 4rem 0;
  background: #F7FAFC;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.details-card {
  background: white;
  border-radius: 16px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

.card-header {
  background: #1A365D;
  color: white;
  padding: 2rem;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-content h2 {
  font-size: 2rem;
  margin: 0;
}

.market-stats {
  display: flex;
  gap: 2rem;
}

.stat {
  text-align: center;
}

.stat-label {
  display: block;
  font-size: 0.875rem;
  opacity: 0.8;
  margin-bottom: 0.25rem;
}

.stat-value {
  font-size: 1.5rem;
  font-weight: 600;
}

.card-body {
  padding: 2rem;
}

.section {
  margin-bottom: 3rem;
}

.section:last-child {
  margin-bottom: 0;
}

.section h3 {
  color: #2D3748;
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
}

.technical-description {
  color: #4A5568;
  font-size: 1.125rem;
  line-height: 1.6;
  margin-bottom: 2rem;
}

.technical-highlights {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.highlight-item {
  display: flex;
  gap: 1rem;
}

.highlight-icon {
  font-size: 1.5rem;
  width: 48px;
  height: 48px;
  background: #EBF8FF;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.highlight-content h4 {
  color: #2D3748;
  margin-bottom: 0.5rem;
}

.highlight-content p {
  color: #718096;
  font-size: 0.875rem;
  line-height: 1.6;
}

.implementation-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.implementation-item {
  background: #F7FAFC;
  padding: 1.5rem;
  border-radius: 12px;
}

.implementation-item h4 {
  color: #2D3748;
  margin-bottom: 1rem;
  font-size: 1.125rem;
}

.implementation-item ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.implementation-item li {
  color: #4A5568;
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
  font-size: 0.875rem;
}

.implementation-item li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: #4299E1;
}

.metrics-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.metric-card {
  background: #F7FAFC;
  padding: 1.5rem;
  border-radius: 12px;
  text-align: center;
}

.metric-card .metric-value {
  display: block;
  font-size: 2rem;
  font-weight: 700;
  color: #4299E1;
  margin-bottom: 0.5rem;
}

.metric-card .metric-label {
  display: block;
  font-size: 1rem;
  color: #2D3748;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.metric-card .metric-description {
  display: block;
  font-size: 0.875rem;
  color: #718096;
}

@media (max-width: 1024px) {
  .technical-highlights {
    grid-template-columns: repeat(2, 1fr);
  }

  .implementation-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .metrics-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .application-details {
    padding: 2rem 0;
  }

  .container {
    padding: 0 1rem;
  }

  .header-content {
    flex-direction: column;
    text-align: center;
    gap: 1.5rem;
  }

  .market-stats {
    justify-content: center;
  }

  .technical-highlights {
    grid-template-columns: 1fr;
  }

  .implementation-grid {
    grid-template-columns: 1fr;
  }

  .metrics-grid {
    grid-template-columns: 1fr;
  }

  .highlight-item {
    align-items: center;
  }

  .card-header {
    padding: 1.5rem;
  }

  .card-body {
    padding: 1.5rem;
  }

  .header-content h2 {
    font-size: 1.75rem;
  }

  .section h3 {
    font-size: 1.25rem;
  }

  .technical-description {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .market-stats {
    flex-direction: column;
    gap: 1rem;
  }

  .highlight-item {
    flex-direction: column;
    text-align: center;
  }

  .highlight-icon {
    margin: 0 auto 1rem;
  }

  .implementation-item {
    padding: 1rem;
  }

  .metric-card {
    padding: 1rem;
  }
}
</style>