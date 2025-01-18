<template>
    <div class="about-bioshuttle">
      <div class="container">
        <section class="about-section">
          <div class="section-header">
            <h1>About BioShuttle</h1>
            <p class="section-subtitle">
              Revolutionizing Therapeutic Compound Delivery
            </p>
          </div>
  
          <div class="about-content">
            <div class="content-column">
              <p>
                BioShuttle is a groundbreaking drug delivery platform developed by Lipotope Holdings, LLC, 
                designed to revolutionize how therapeutic compounds are transported throughout the body. 
                Our proprietary technology utilizes stabilized liposomes to overcome traditional barriers 
                in drug delivery, enabling unprecedented access to previously challenging biological targets.
              </p>
            </div>
            
            <div class="content-column">
              <p>
                At the core of our innovation is the ability to dramatically improve drug bioavailability, 
                reduce dosing requirements, and provide safe, efficient transportation of therapeutic 
                compounds across complex biological barriers, including the blood-brain barrier. 
                This breakthrough technology has the potential to transform treatment approaches 
                in multiple therapeutic areas, from neurological disorders to cancer treatment.
              </p>
            </div>
          </div>
  
          <div class="about-highlights">
            <div class="highlight-card">
              <div class="highlight-icon">🧬</div>
              <div class="highlight-content">
                <h4>Innovative Delivery</h4>
                <p>Proprietary liposomal technology that overcomes biological barriers</p>
              </div>
            </div>
  
            <div class="highlight-card">
              <div class="highlight-icon">🔬</div>
              <div class="highlight-content">
                <h4>Enhanced Bioavailability</h4>
                <p>Reduced dosing with improved therapeutic effectiveness</p>
              </div>
            </div>
  
            <div class="highlight-card">
              <div class="highlight-icon">🌐</div>
              <div class="highlight-content">
                <h4>Versatile Applications</h4>
                <p>Transformative potential across multiple therapeutic domains</p>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </template>
  
  <script setup>
  // No dynamic logic required for this component
  </script>
  
  <style scoped>
  .about-bioshuttle {
    padding: 6rem 0;
    background: #F7FAFC;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }
  
  .section-header {
    text-align: center;
    margin-bottom: 4rem;
  }
  
  .section-header h1 {
    color: #1A365D;
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }
  
  .section-subtitle {
    color: #4A5568;
    font-size: 1.25rem;
    line-height: 1.6;
  }
  
  .about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-bottom: 4rem;
  }
  
  .content-column p {
    color: #2D3748;
    line-height: 1.8;
    margin-bottom: 1rem;
  }
  
  .about-highlights {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
  
  .highlight-card {
    background: white;
    border-radius: 16px;
    padding: 2rem;
    display: flex;
    align-items: center;
    gap: 1.5rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .highlight-card:hover {
    transform: translateY(-5px);
  }
  
  .highlight-icon {
    font-size: 3rem;
    width: 80px;
    height: 80px;
    background: #EDF2F7;
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .highlight-content h4 {
    color: #2D3748;
    font-size: 1.25rem;
    margin-bottom: 0.5rem;
  }
  
  .highlight-content p {
    color: #4A5568;
    line-height: 1.6;
  }
  
  @media (max-width: 1024px) {
    .about-content,
    .about-highlights {
      grid-template-columns: 1fr;
    }
  
    .container {
      padding: 0 1.5rem;
    }
  }
  
  @media (max-width: 768px) {
    .about-bioshuttle {
      padding: 4rem 0;
    }
  
    .section-header h1 {
      font-size: 2rem;
    }
  
    .highlight-card {
      flex-direction: column;
      text-align: center;
    }
  }
  </style>