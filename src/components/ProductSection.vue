<template>
  <!-- Coffee Section -->
  <section class="product-section" id="coffee">
    <h3>Our Special Coffee</h3>
    <div class="product-grid">
      <div
        class="product-card"
        v-for="(coffee, index) in coffeeList"
        :key="index"
      >
        <img :src="coffee.img" :alt="coffee.name" class="product-image" />
        <div class="product-info">
          <h4>{{ coffee.name }}</h4>
          <p>{{ coffee.price }}</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Dessert Section -->
  <section class="product-section" id="dessert">
    <h3>Our Special Dessert</h3>
    <div class="product-grid">
      <div
        class="product-card"
        v-for="(dessert, index) in dessertList"
        :key="index"
      >
        <img :src="dessert.img" :alt="dessert.name" class="product-image" />
        <div class="product-info">
          <h4>{{ dessert.name }}</h4>
          <p>{{ dessert.price }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const coffeeList = [
  {
    img: "/src/assets/coffe/lungo_coffe.jpeg",
    name: "Lungo Coffee",
    price: "Rs. 199",
  },
  {
    img: "/src/assets/coffe/dalgona_coffe.jpeg",
    name: "Dalgona Coffee",
    price: "Rs. 159",
  },
  {
    img: "/src/assets/coffe/iced_coffee.jpeg",
    name: "Iced Coffee",
    price: "Rs. 149",
  },
  {
    img: "/src/assets/coffe/filter_coffe.jpeg",
    name: "Filter Coffee",
    price: "Rs. 99",
  },
];

const dessertList = [
  {
    img: "/src/assets/dessert/gulap_jamun.jpeg",
    name: "Gulab Jamun",
    price: "Rs. 199",
  },
  {
    img: "/src/assets/dessert/chocolato_.tiramisu.jpeg",
    name: "Chocolate Tiramisu",
    price: "Rs. 250",
  },
  {
    img: "/src/assets/dessert/churros.jpeg",
    name: "Churros",
    price: "Rs. 170",
  },
  {
    img: "/src/assets/dessert/australian_lamingtons.jpeg",
    name: "Australian Lamingtons",
    price: "Rs. 280",
  },
];
</script>

<style scoped>
.product-section {
  padding: 2rem 1rem;
}

.product-section h3 {
  text-align: center;
  font-size: 1.8rem;
  margin-bottom: 2rem;
  color: #333;
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.product-card {
  background-color: #fff;
  border-radius: 0.75rem;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.product-card:hover {
  transform: translateY(-8px);
}

.product-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.product-info {
  padding: 1rem;
  text-align: center;
}

.product-info h4 {
  margin: 0 0 0.5rem;
  font-size: 1.2rem;
  color: #222;
}

.product-info p {
  margin: 0;
  color: #6b4f4f;
  font-weight: bold;
  font-size: 1rem;
}
</style>
