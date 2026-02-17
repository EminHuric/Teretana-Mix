<template>
  <footer class="site-footer">
    <div class="footer-container">
      <!-- LEVI DEO: Logo i opis -->
      <div class="footer-left">
        <img src="/logo.png" alt="Logo" class="footer-logo">
        <p>Otvorena 2008. godine, premium teretana sa preko 5000 zadovoljnih članova.</p>
      </div>

      <!-- SREDNJI DEO: Navigacija -->
      <div class="footer-center">
        <h4>Brza Navigacija</h4>
        <ul>
          <li><a href="#o-nama">O nama</a></li>
          <li><a href="#gallery">Slike</a></li>
          <li><a href="#cenovnik">Cenovnik</a></li>
          <li><a href="#lokacija">Lokacija</a></li>
          <li><a href="#kontakt">Kontakt</a></li>
        </ul>
      </div>

      <!-- DESNI DEO: Kontakt -->
      <div class="footer-right">
        <h4>Kontakt</h4>
        <p>Email: <a href="mailto:markotara.pp@gmail.com">markotara.pp@gmail.com</a></p>
        <p>Telefon: +381 65 2206269</p>
        <p>Ulica Snadžackih Brigada 7</p>
      </div>
    </div>

    <!-- DONJI DEO: copyright -->
    <div class="footer-bottom">
      <p>© 2026 Premium Teretana. Sva prava zadržana.</p>
    </div>
  </footer>
</template>

<script setup>
// Footer je statičan, JS nije potreban
</script>

<style scoped>
.site-footer {
  background-color: #000;
  color: #fff;
  padding: 50px 20px 20px;
  font-family: Arial, Helvetica, sans-serif;
}

.footer-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  max-width: 1200px;  /* ograničava širinu na velikim ekranima */
  margin: 0 auto;      /* centrirano */
  gap: 40px;
}

.footer-left,
.footer-center,
.footer-right {
  flex: 1;
  min-width: 250px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.footer-left {
  text-align: left;
}

.footer-logo {
  height: 80px;
  margin-bottom: 15px;
  border-radius: 50%;
  border: 3px solid #FFD700;
}

.footer-left p {
  font-size: 16px;
  line-height: 1.5;
}

.footer-center h4,
.footer-right h4 {
  color: #FFD700;
  margin-bottom: 12px;
  font-size: 18px;
}

.footer-center ul {
  list-style: none;
  padding: 0;
}

.footer-center ul li {
  margin-bottom: 10px;
}

.footer-center ul li a {
  color: #FFD700;
  text-decoration: none;
  transition: 0.3s;
}

.footer-center ul li a:hover {
  text-decoration: underline;
}

.footer-right p a {
  color: #FFD700;
  text-decoration: none;
}

.footer-bottom {
  text-align: center;
  border-top: 1px solid #FFD700;
  margin-top: 30px;
  padding-top: 15px;
  font-size: 14px;
}

/* RESPONSIVE */
@media (max-width: 1024px) {
  .footer-container {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .footer-left,
  .footer-center,
  .footer-right {
    align-items: center;
  }
}
</style>
