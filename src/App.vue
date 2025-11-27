<script setup>
import { RouterView } from "vue-router";
import foodFest from "@/assets/cape food.jpg";
import TierList from "./components/TierList.vue";
</script>

<template>
  <main>
    <section>
      <img id="food" :src="foodFest" />
      <h1>Welcome to the Food Fest 2025</h1>
      <p>
        the ultimate day out for food lovers! From gourmet street bites to bold flavour experiments,
      </p>
      <p>
        this festival is packed with good vibes, live music, local vendors, and unforgettable
        tastes.
      </p>

      <h2>What To Expect</h2>
      <p>40+ curated food and drink vendors</p>
      <p>Live cooking demonstrations from local chefs</p>
      <p>Craft beer, cocktail bars, and specialty drink stands</p>
      <p>Chill zones, picnic areas, and shaded seating</p>
      <p>Live performances throughout the day</p>

      <h2>Festival Highlights</h2>
      <p>Chef Showcase Stage – see chefs cook live</p>
      <p>Taste Trail – sample signature bites from multiple vendors</p>
      <p>Sweet Lane – all things dessert</p>
      <p>Braai & Smokehouse Section – flame-grilled favourites</p>

      <h2>Event Details</h2>
      <p>Date: 21–23 March 2025</p>
      <p>Time: 10:00 – 20:00</p>
      <p>Location: Green Point Park, Cape Town</p>
      <p></p>
    </section>

    <TierList />
  </main>
  <RouterView />
</template>

<style scoped>
#food {
  margin-top: 2rem;
  object-fit: cover;

  width: 600px;
  overflow: hidden;
}
main {
  display: flex;
  justify-content: center;
  margin: auto;
}
</style>
