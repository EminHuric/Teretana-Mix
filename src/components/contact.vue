<template>
  <section class="contact-section">
    <!-- LEVO: Kontakt forma -->
    <div class="contact-left" id="kontakt">
      <h3>Kontaktirajte Nas</h3>
      <form :action="'mailto:markotara.pp@gmail.com'" method="post" enctype="text/plain">
        <input type="text" name="Ime" placeholder="Ime" required />
        <input type="email" name="Email" placeholder="Email" required />
        <textarea name="Poruka" placeholder="Poruka" required></textarea>
        <button type="submit">Pošalji</button>
      </form>
    </div>

    <!-- CENTAR: uspravna linija -->
    <div class="center-line"></div>

    <!-- DESNO: Lokacija -->
    <div class="contact-right" id="lokacija">
      <h3>Lokacija</h3>
      <p>Ulica Snadžackih Brigada 7</p>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2897.5820885136746!2d19.65551727617786!3d43.39236097913681!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x475d1092c16b7f2b%3A0x0!2zNDPCsDIzJzM3LjYiTiAxOcKwMzknMDUuMCJF!5e0!3m2!1sen!2srs!4v1700000000000!5m2!1sen!2srs"
        width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"
      ></iframe>
    </div>
  </section>
</template>

<script setup>
// Nema dodatnog JS-a, forma radi preko mailto
</script>

<style scoped>
.contact-section {
  display: flex;
  justify-content: center;
  align-items: center; /* ravnomerno po visini */
  gap: 60px;
  padding: 60px 20px;
  background-color: #000;
  color: white;
  flex-wrap: wrap;
  min-height: 500px; /* da linija bude centrirana */
}

/* LEVO: Kontakt forma */
.contact-left {
  flex: 1;
  min-width: 300px;
  max-width: 450px;
  background-color: #000;
  padding: 30px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  justify-content: center;
  align-items: center;
}

.contact-left h3 {
  color: #FFD700;
  font-size: 28px;
  margin-bottom: 10px;
}

.contact-left form {
  display: flex;
  flex-direction: column;
  gap: 15px;
  width: 100%;
}

.contact-left input,
.contact-left textarea {
  padding: 12px;
  border-radius: 10px;
  border: 2px solid #FFD700;
  background-color: #000;
  color: white;
  font-size: 16px;
  width: 100%;
}

.contact-left input::placeholder,
.contact-left textarea::placeholder {
  color: #ccc;
}

.contact-left button {
  padding: 12px;
  background-color: #FFD700;
  color: #000;
  font-weight: bold;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.contact-left button:hover {
  background-color: #e6c200;
}

.center-line {
  width: 4px;
  background-color: #fad400;
  height: 80%; /* stoji ravnomerno između form-e i mape */
  align-self: center;
  border: 1px solid #fad400;
  height: 450px;
  margin-top: 200px;
}

/* DESNO: Lokacija */
.contact-right {
  flex: 1;
  min-width: 300px;
  max-width: 450px;
  background-color: #000;
  padding: 30px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  justify-content: center;
  align-items: center;
}

.contact-right h3 {
  color: #FFD700;
  font-size: 28px;
  margin-top: 100px;
}

.contact-right p {
  font-size: 18px;
  margin-bottom: 10px;
  color: #fff;
}

.contact-right iframe {
  border-radius: 12px;
  border: 2px solid #FFD700;
  width: 100%;
  max-width: 450px;
}

/* Responsive */
@media (max-width: 1024px) {
  .contact-section {
    flex-direction: column;
    align-items: center;
  }
  .center-line {
    width: 80%;
    height: 4px;
    margin: 20px 0;
  }
  .contact-left,
  .contact-right {
    width: 70%;
  }
}
</style>
