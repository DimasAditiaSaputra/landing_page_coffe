<script setup>
import Navbar from "./components/Navbar.vue";
import WelcomeSection from "./components/WelcomeSection.vue";
import ProductSection from "./components/ProductSection.vue";
import Footer from "./components/Footer.vue";
</script>
<template>
  <Navbar />
  <main>
    <div class="welcome-section">
      <WelcomeSection />
    </div>
    <ProductSection />
    <Footer />
  </main>
</template>
<style></style>
