<template>
  <section class="gallery" id="slike">
    <h2>Naš Prostor</h2>

    <div class="slider">
      <div class="track">
        <!-- Duplirane slike da bi scroll bio beskonačan -->
        <div v-for="n in 2" :key="n" class="grid">
          <img src="/1.jpeg" />
          <img src="/2.jpeg" />
          <img src="/3.jpeg" />
          <img src="/4.jpeg" />
          <img src="/5.jpeg" />
          <img src="/6.jpeg" />
          <img src="/7.jpeg" />
          <img src="/8.jpeg" />
          <img src="/9.jpeg" />
          <img src="/10.jpeg" />
          <img src="/11.jpeg" />
          <img src="/12.jpeg" />
          <img src="/13.jpeg" />
          <img src="/14.jpeg" />
          <img src="/15.jpeg" />
          <img src="/16.jpeg" />
          <img src="/17.jpeg" />
          <img src="/18.jpeg" />
          <img src="/19.jpeg" />
          <img src="/20.jpeg" />
          <img src="/21.jpeg" />
          <img src="/22.jpeg" />
          <img src="/23.jpeg" />
          <img src="/24.jpeg" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Nema JS logike — sve radi CSS animacija
</script>

<style scoped>
.gallery {
  background: #000;
  padding: 60px 0;
  overflow: hidden;
  text-align: center;
  color: #FFD700;
}

.gallery h2 {
  font-size: 42px;
  margin-bottom: 40px;
}

/* Slider */
.slider {
  overflow: hidden;
  width: 100%;
}

/* Track */
.track {
  display: flex;
  width: fit-content;
  animation: scroll 40s linear infinite;
}

/* Grid u 2 reda */
.grid {
  display: grid;
  grid-template-rows: repeat(2, 320px);
  grid-auto-flow: column;
  gap: 20px;
  padding: 0 10px; /* 10px levo i desno */
}

/* Slike */
.grid img {
  width: 500px;
  height: 320px;
  object-fit: cover;
  border-radius: 16px;
  margin: 10px; /* minimum 10px razmak svuda */
}

/* PRVA SLIKA VEĆA */
.grid img:first-child {
  width: 650px;
  height: 400px;
}

/* Uklonjen hover zoom */
.grid img:hover {
  transform: none;
}

/* Animacija */
@keyframes scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}

/* Responsive */
@media (max-width: 768px) {
  .grid {
    grid-template-rows: repeat(2, 180px);
  }

  .grid img {
    width: 250px;
    height: 180px;
  }

  .grid img:first-child {
    width: 320px;
    height: 220px;
  }
}

</style>
