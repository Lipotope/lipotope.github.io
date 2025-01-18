<template>
    <div class="mobile-menu">
      <!-- Hamburger Button -->
      <button 
        class="menu-toggle" 
        @click="toggleMenu"
        aria-label="Toggle menu"
      >
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
      </button>
  
      <!-- Mobile Navigation -->
      <Transition name="menu">
        <div v-if="isOpen" class="mobile-nav">
          <!-- Menu Header -->
          <div class="menu-header">
            <span>Menu</span>
            <button 
              class="close-button" 
              @click="closeMenu"
              aria-label="Close menu"
            >
              ✕
            </button>
          </div>
  
          <!-- Menu Links -->
          <div class="menu-content">
            <NuxtLink 
              v-for="item in navigationItems" 
              :key="item.path"
              :to="item.path"
              class="menu-link"
              :class="{ active: item.path !== '/' && route.path === item.path }"
              @click="closeMenu"
            >
              {{ item.label }}
            </NuxtLink>
          </div>
        </div>
      </Transition>
  
      <!-- Overlay -->
      <Transition name="fade">
        <div v-if="isOpen" class="menu-overlay" @click="closeMenu"></div>
      </Transition>
    </div>
  </template>
  
  <script setup>
  const isOpen = ref(false)
  const route = useRoute()
  
  const navigationItems = [
    { path: '/', label: 'Home' },
    { path: '/technology', label: 'Technology' },
    { path: '/applications', label: 'Applications' },
    { path: '/products', label: 'Products' },
    { path: '/about', label: 'About' },
    { path: '/contact', label: 'Contact' }
  ]
  
  const toggleMenu = () => {
    isOpen.value = !isOpen.value
    if (process.client) {
      document.body.style.overflow = isOpen.value ? 'hidden' : ''
    }
  }
  
  const closeMenu = () => {
    isOpen.value = false
    if (process.client) {
      document.body.style.overflow = ''
    }
  }
  
  // Watch for route changes to close menu
  watch(() => route.path, () => {
    closeMenu()
  })
  
  // Ensure body overflow is reset when component is unmounted
  onUnmounted(() => {
    if (process.client) {
      document.body.style.overflow = ''
    }
  })
  </script>
  
  <style scoped>
  .mobile-menu {
    position: relative;
    z-index: 1000;
  }
  
  .menu-toggle {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 6px;
    width: 24px;
    height: 24px;
    padding: 0;
    background: none;
    border: none;
    cursor: pointer;
  }
  
  .hamburger-line {
    width: 100%;
    height: 2px;
    background-color: #1a365d;
    transition: all 0.3s ease;
  }
  
  .mobile-nav {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #1a365d;
    z-index: 1001;
    display: flex;
    flex-direction: column;
  }
  
  .menu-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem;
    color: white;
    font-size: 1.25rem;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .close-button {
    background: none;
    border: none;
    color: white;
    font-size: 1.5rem;
    padding: 0.5rem;
    cursor: pointer;
  }
  
  .menu-content {
    flex-grow: 1;
    padding: 2rem 1.5rem;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }
  
  .menu-link {
    display: block;
    color: white;
    text-decoration: none;
    font-size: 1.5rem;
    padding: 1rem;
    border-radius: 8px;
    transition: background-color 0.2s ease;
  }
  
  .menu-link:hover {
    background: rgba(255, 255, 255, 0.1);
  }
  
  .menu-link.active {
    background: #4299e1;
  }
  
  /* Transitions */
  .menu-enter-active,
  .menu-leave-active {
    transition: transform 0.3s ease;
  }
  
  .menu-enter-from,
  .menu-leave-to {
    transform: translateY(100%);
  }
  
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.3s ease;
  }
  
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
  
  @media (min-width: 769px) {
    .mobile-menu {
      display: none;
    }
  }
  </style>