<script setup>
import LikeBtn from "./LikeBtn.vue";


const TierCards = [
  {
    id: 1,
    name: "VIP Experience",
    description: [
      "Fast-track entrance",
      "Access to VIP lounge",
      "2 complimentary food tastings",
      "Front-row access to live cooking demos",
      "Exclusive festival merch"
    ],
    price: "R299.00",
  },
  {
     id: 2,
    name: "Standard Pass",
    description: [
      "Full-day festival access",
      "Access to all food stalls",
      "Live music included",
      "Entry to general seating areas"
    ],
    price: "R149.00",
  },
  {
     id: 3,
    name: "Budget Entry",
    description: [
      "General admission",
      "Access to food stalls",
      "Limited seating areas"
    ],
    price: "R79.00",
  }
];
</script>

<template>
  <div class="tier-list">
    <div
      v-for="(card, index) in TierCards"
      :key="card.id"
      :class="['card', { 'featured-card': index === 1 , 'VIP-card': index===0}]"

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
.card:hover{
  transform: scale(1.05);
}
.featured-card {
  transform: scale(1.0);
  box-shadow: 0 0.5rem 1.5rem rgba(0, 0, 0, 0.3);
  border: 2px solid #a06ce4;
}
.VIP-card{
   border: 2px solid #e1b12c;
}
.card-body{
  padding: 2rem;
}
</style>
