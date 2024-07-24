<!-- src/components/FishCalculator.vue -->
<template>
  <div class="calculator-container">
    <h1 class="title">Perhitungan Perikanan</h1>
    <div class="input-group">
      <label for="fishCount">Jumlah Ikan:</label>
      <input id="fishCount" v-model.number="fishCount" type="number" />
    </div>
    <div class="input-group">
      <label for="fishWeight">Berat Ikan per ekor (kg):</label>
      <input id="fishWeight" v-model.number="fishWeight" type="number" />
    </div>
    <button @click="calculateTotalWeight">Hitung</button>
    <h2 class="result">Total Berat: {{ totalWeight }} kg</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fishCount: 0,
      fishWeight: 0,
      totalWeight: 0,
    };
  },
  methods: {
    calculateTotalWeight() {
      this.totalWeight = this.fishCount * this.fishWeight;
    },
  },
};
</script>

<style scoped>
.calculator-container {
  max-width: 500px;
  margin: 0 auto;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  background: #fff;
}

.title {
  font-size: 2rem;
  margin-bottom: 1rem;
  color: #333;
}

.input-group {
  margin-bottom: 1rem;
}

.input-group label {
  display: block;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.input-group input {
  width: 100%;
  padding: 0.5rem;
  font-size: 1rem;
  border: 1px solid #ddd;
  border-radius: 5px;
}

button {
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  color: #fff;
  background-color: #007bff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #0056b3;
}

.result {
  margin-top: 1rem;
  font-size: 1.25rem;
  color: #333;
}
</style>
