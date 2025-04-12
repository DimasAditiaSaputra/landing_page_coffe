<script setup></script>
<template>
  <section class="welcome-section" id="home">
    <h2>Welcome!</h2>
    <p>We serve the richest coffee in the city!</p>
    <button class="btn">Click Here</button>
  </section>
</template>
<style>
.welcome-section {
  text-align: center;
  width: 100%;
  height: 34rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-image: url("/src/assets/bg/bg_coffee.jpeg");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  background-position: center;
}

.welcome-section h2 {
  font-size: 2rem;
  margin-bottom: 0.5rem;
}

.welcome-section p {
  color: beige;
}

.btn {
  background-color: #6b4f4f;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 0.25rem;
  cursor: pointer;
  font-size: 1rem;
  transition: background-color 0.3s;
}

.btn:hover {
  background-color: #5a4242;
}
</style>
