<script setup>
import LikeBtn from "./LikeBtn.vue";


const TierCards = [
  {
    id: 1,
    name: "premium",
    description: [
      "This is the best tier",
      "Live music",
      "Exclusive seating",
      "VIP support"
    ],
    price: "R99.99",
  },
  {
    id: 2,
    name: "standard",
    description: "This is the standard tier",
    price: "R59.99",
  },
  {
    id: 3,
    name: "budget",
    description: "This is the budget tier",
    price: "R29.99",
  },
];
</script>

<template>
  <div class="tier-list">
    <div
      v-for="(card, index) in TierCards"
      :key="card.id"
      :class="['card', { 'featured-card': index === 1 }]"
      style="width: 20rem; height: 24rem"
    >
      <div class="card-body">
          <div class=" d-flex justify-content-between mb-2rem">
              <h5 class="card-title">{{ card.name }}</h5>
              <LikeBtn />
        </div>
      
        <li v-for="(item,i) in card.description" :key="i" class="card-subtitle mb-2 text-body-secondary">{{ item }}</li>
        <p class="card-text">{{ card.price }}</p>
        <button class="btn btn-primary">Select</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.tier-list {
  
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
 
}

.card {
  margin: 1rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.featured-card {
  transform: scale(1.05);
  box-shadow: 0 0.5rem 1.5rem rgba(0, 0, 0, 0.3);
  border: 2px solid #ffc107;
}
</style>
