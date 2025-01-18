<template>
    <header class="header">
      <div class="container">
        <div class="header-content">
          <NuxtLink to="/" class="logo-link">
           <img class="logo-image" src="../public/logo_transparent.png" alt=""> <span class="logo-text">BioShuttle</span>
          </NuxtLink>
          
          <nav class="main-nav">
            <NuxtLink 
              to="/" 
              class="nav-link home-link"
            >
              Home
            </NuxtLink>
            <NuxtLink 
              to="/technology" 
              class="nav-link" 
              :class="{ active: route.path === '/technology' }"
            >
              Technology
            </NuxtLink>
            <NuxtLink 
              to="/applications" 
              class="nav-link" 
              :class="{ active: route.path === '/applications' }"
            >
              Applications
            </NuxtLink>
            <NuxtLink 
              to="/products" 
              class="nav-link" 
              :class="{ active: route.path === '/products' }"
            >
              Products
            </NuxtLink>
            <NuxtLink 
              to="/about" 
              class="nav-link" 
              :class="{ active: route.path === '/about' }"
            >
              About
            </NuxtLink>
            <NuxtLink 
              to="/contact" 
              class="nav-link contact-link" 
              :class="{ active: route.path === '/contact' }"
            >
              Contact
            </NuxtLink>
          </nav>
  
          <MobileMenu class="mobile-menu-component" />
        </div>
      </div>
    </header>
  </template>
  
  <script setup>
  import MobileMenu from './MobileMenu.vue'
  
  const route = useRoute()
  </script>
  
  <style scoped>
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1000;
    background: rgba(255, 255, 255, 0.98);
    backdrop-filter: blur(8px);
    box-shadow: 0 1px 0 rgba(0, 0, 0, 0.1);
    padding: 1rem 0;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
  }
  
  .header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo-link {
    text-decoration: none;
    color: #1a365d;
    display: flex;
    align-items: center;
  }

  .logo-image {
    width: 2rem
  }
  
  .logo-text {
    font-size: 1.5rem;
    font-weight: 700;
    letter-spacing: -0.5px;
  }
  
  .main-nav {
    display: flex;
    gap: 2rem;
    align-items: center;
  }
  
  .nav-link {
    text-decoration: none;
    color: #4a5568;
    font-weight: 500;
    font-size: 1rem;
    padding: 0.5rem;
    transition: all 0.2s ease;
    position: relative;
  }
  
  .nav-link:hover {
    color: #1a365d;
  }
  
  .nav-link::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 100%;
    height: 2px;
    background: #4299e1;
    transform: scaleX(0);
    transition: transform 0.2s ease;
  }
  
  /* Remove underline effect for home link */
  .home-link::after {
    display: none;
  }
  
  .nav-link:hover::after,
  .nav-link.active::after {
    transform: scaleX(1);
  }
  
  .contact-link {
    background: #4299e1;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 6px;
  }
  
  .contact-link:hover {
    background: #2b6cb0;
    color: white;
  }
  
  .contact-link::after {
    display: none;
  }
  
  .mobile-menu-component {
    display: none;
  }
  
  @media (max-width: 768px) {
    .header {
      padding: 1rem;
    }
  
    .main-nav {
      display: none;
    }
  
    .mobile-menu-component {
      display: block;
    }
  }
  </style>