<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);

const openMenu = () => {
  isMenuOpen.value = true;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};
</script>

<template>
  <header>
    <div class="container header-container">
      <div class="logo">Coffee</div>

      <nav class="desktop-menu">
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#coffee">Coffee</a></li>
          <li><a href="#dessert">Dessert</a></li>
        </ul>
      </nav>

      <!-- Hamburger button -->
      <button class="mobile-menu-btn" @click="openMenu">
        <i class="fas fa-bars"></i>
      </button>
    </div>

    <!-- Mobile menu -->
    <div class="mobile-menu" :class="{ active: isMenuOpen }">
      <button class="close-menu" @click="closeMenu">
        <i class="fas fa-times"></i>
      </button>
      <nav>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#coffee">Coffee</a></li>
          <li><a href="#dessert">Dessert</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
header {
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 100%;
  position: fixed;
  z-index: 999;
}

.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

nav ul {
  display: flex;
  list-style: none;
  gap: 1rem;
}

nav a {
  text-decoration: none;
  color: #4a4a4a;
  transition: color 0.3s;
}

nav a:hover {
  color: #6b4f4f;
}

.mobile-menu-btn {
  display: none;
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #4a4a4a;
}

/* Mobile menu */
.mobile-menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.9);
  z-index: 100;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transform: translateX(-100%);
  transition: transform 0.3s ease-in-out;
}

.mobile-menu.active {
  transform: translateX(0);
}

.mobile-menu ul {
  display: flex;
  flex-direction: column;
  text-align: center;
}

.mobile-menu li {
  margin: 1rem 0;
}

.close-menu {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
}

/* Responsive rules */
@media (max-width: 768px) {
  .desktop-menu {
    display: none;
  }

  .mobile-menu-btn {
    display: block;
  }
}
</style>
