<template>
  <section class="about" id="o-nama">
    <div class="content">
      <h2>O nama</h2>
      <p>
        Naša teretana je otvorena u oktobru 2008. godine sa jasnom vizijom – da pružimo vrhunski trening, profesionalnu podršku i prostor u kojem svaki član može da postane najbolja verzija sebe. Kroz više od jedne decenije rada, više od <strong>5000 zadovoljnih članova</strong> je prošlo kroz naš prostor i iskusilo kvalitet, posvećenost i motivaciju koji nas čine jedinstvenima u gradu. Naša misija je da nastavimo da inspirišemo, pomažemo i gradimo zajednicu ljudi koji žele da ulažu u svoje zdravlje i snagu.
      </p>
    </div>
  </section>
</template>

<script setup>
// Za sada nema logike, samo statični sadržaj
</script>

<style scoped>
.about {
  padding: 100px 20px;
  background-color: #000; /* crna pozadina */
 
  display: flex;
  justify-content: center;
  text-align: center;
}

.content {
  max-width: 900px;
}

.about h2 {
  font-size: 48px;
  margin-bottom: 30px;
  font-weight: bold;
   color: #FFD700; 
}

.about p {
  font-size: 20px;
  line-height: 1.8;
   color: #ffffff; 
   font-family: Arial, Helvetica, sans-serif;
   font-size: 22px;

}

/* Responsive */
@media (max-width: 768px) {
  .about {
    padding: 60px 15px;
  }

  .about h2 {
    font-size: 36px;
  }

  .about p {
    font-size: 18px;
  }
}

@media (max-width: 480px) {
  .about h2 {
    font-size: 28px;
  }

  .about p {
    font-size: 16px;
  }
}
</style>
