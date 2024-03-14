<template>
  <div class="container">
    <h1 class="title">Gleap Nuxt Example</h1>
    <button @click="openWidget" class="centered-button">Open Gleap widget</button>
    <button @click="openFeatureArticle" class="centered-button">Open article</button>
  </div>
</template>

<script setup>
import Gleap from 'gleap';

// Initializing Gleap
Gleap.initialize("ogWhNhuiZcGWrva5nlDS8l7a78OfaLlV");

function openWidget() {
  Gleap.open();
}

function openFeatureArticle() {
   Gleap.openHelpCenterArticle("127", false);
}
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.title {
  margin-bottom: 20px;
}

.centered-button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  margin-bottom: 20px;
  border: none;
  border-radius: 5px;
  background-color: #2142E7;
  color: white;
  transition: background-color 0.3s ease;

}

.centered-button:hover {
  background-color: #0056b3;
}
</style>
