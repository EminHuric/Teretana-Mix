<template>
  <section class="pricing">
    <h2>Naš Cenovnik</h2>
    <p class="subtitle">Radno vreme: Pon-Sub 9-22h | Nedeljom zatvoreno</p>

    <div class="cards">
      <div class="card" v-for="plan in plans" :key="plan.name">
        <div class="badge" v-if="plan.popular">Najpopularniji</div>
        <h3>{{ plan.name }}</h3>
        <p class="price">
          <span class="amount">{{ plan.price }}</span> <span class="period">{{ plan.period }}</span>
        </p>
        <ul>
          <li v-for="item in plan.details" :key="item">{{ item }}</li>
        </ul>
        <a href="#kontakt"><button>Zakaži</button></a>
      </div>
    </div>
  </section>
  
<section class="bonus-box">
  <div class="box">
    <div class="circle">
      <span>GRATIS</span>
    </div>
    <p class="bonus-text">Profesionalna obuka za muškarce i žene</p>
  </div>
</section>



</template>

<script setup>
const plans = [
  {
    name: "Teretana",
    price: "2000 RSD",
    period: "mesečno",
    details: ["Neograničen broj dolazaka", "Pristup teretani"],
  },
  {
    name: "Teretana + traka",
    price: "2500 RSD",
    period: "mesečno",
    details: ["Neograničen broj dolazaka", "Pristup traci", "Premium oprema"],
    popular: true
  },
  {
    name: "Termin",
    price: "200 RSD",
    period: "po terminu",
    details: ["Sa trakom 300 RSD", "Bez ograničenja u terminima"],
  },
]


</script>

<style scoped>
.bonus-box {
  display: flex;
  justify-content: center;
  margin: -40px 20px;
}

.box {
  background-color: #000000; /* tamni kvadrat */
  padding: 40px;
  border: 5px solid #FFD700; /* zlatni okvir kvadrata */
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 400px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.6);
}

.circle {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  background-color: #000; /* crno unutra */
  border: 6px solid #FFD700; /* zlatni okvir kruga */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
  transition: transform 0.3s ease;
}

.circle span {
  font-size: 36px;
  font-weight: bold;
  color: #FFD700;
  text-transform: uppercase;
}

.circle:hover {
  transform: scale(1.1);
}

.bonus-text {
  font-size: 22px;
  color: #FFD700;
  font-weight: bold;
  text-align: center;
}




.pricing {
  background: linear-gradient(135deg, #000, #000000);
  color: #FFD700;
  text-align: center;
  padding: 80px 20px;
}

.pricing h2 {
  font-size: 50px;
  margin-bottom: 10px;
}

.subtitle {
  font-size: 18px;
  margin-bottom: 50px;
  color: #ccc;
}

.cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 40px;
}

.card {
  background: #111;
  border: 2px solid #FFD700;
  border-radius: 20px;
  padding: 30px 25px;
  width: 300px;
  position: relative;
  transition: transform 0.4s, box-shadow 0.4s;
}

.card:hover {
  transform: translateY(-15px) scale(1.05);
  box-shadow: 0 15px 30px rgba(255, 215, 0, 0.4);
}

.badge {
  position: absolute;
  top: -15px;
  right: -15px;
  background: #FFD700;
  color: #000;
  padding: 8px 15px;
  font-weight: bold;
  border-radius: 12px;
  font-size: 14px;
}

.card h3 {
  font-size: 28px;
  margin-bottom: 20px;
}

.price {
  font-size: 32px;
  font-weight: bold;
  margin-bottom: 20px;
}

.price .period {
  font-size: 18px;
  font-weight: normal;
  color: #ccc;
}

.card ul {
  list-style: none;
  padding: 0;
  margin-bottom: 25px;
}

.card ul li {
  margin: 10px 0;
  font-size: 16px;
}

.card button {
  background-color: #FFD700;
  color: #000;
  font-weight: bold;
  border: none;
  border-radius: 12px;
  padding: 12px 25px;
  cursor: pointer;
  font-size: 16px;
  transition: background 0.3s;
}

.card button:hover {
  background-color: #e6c200;
}

/* Responsive */
@media (max-width: 1024px) {
  .cards {
    flex-direction: column;
    align-items: center;
  }

  .card {
    width: 80%;
  }
}

@media (max-width: 480px) {
  .pricing h2 {
    font-size: 36px;
  }
  .price {
    font-size: 28px;
  }
}
</style>
