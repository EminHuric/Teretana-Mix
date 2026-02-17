<template>
  <div class="border">
    <!-- Logo vodi na vrh stranice -->
    <a href="#top">
      <img alt="logo" src="/logo.png" class="logo">
    </a>

    <!-- Desktop meni -->
    <a href="#o-nama" class="onama">O nama</a>
    <a href="#slike" class="cenovnik">Slike</a>
    <a href="#cenovnik" class="slike">Cenovnik</a>
    <a href="#lokacija" class="lokacija">Lokacija</a>
    <a href="#kontakt"><button class="kontakt">Kontakt</button></a>

    <!-- Hamburger za mobilni -->
    <button class="menub" @click="toggleMenu">
      <i class="fa-solid fa-bars"></i>
    </button>

    <!-- Overlay meni -->
    <div class="overlay" v-show="menuOpen" @click.self="closeMenu">
      <div class="menu-items">
        <button class="close-btn" @click="closeMenu">X</button>
        <a href="#o-nama" @click="closeMenu">O nama</a>
        <a href="#slike" @click="closeMenu">Slike</a>
        <a href="#cenovnik" @click="closeMenu">Cenovnik</a>
        <a href="#lokacija" @click="closeMenu">Lokacija</a>
        <a href="#kontakt" @click="closeMenu">Kontakt</a>
        
        <img alt="logo1" src="/logo.png" class="lg">
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}

const closeMenu = () => {
  menuOpen.value = false
}

</script>

<style scoped>
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.85);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 99;
  overflow: hidden
}

.menu-items button {
    color: white;
    margin-top: -120px;
    right: 50px;
    font-size: 60px;
    position: absolute;
    background: none;
    color: rgb(255, 230, 0);
    border: none;
}
.menub {
    display: none;
}
.menu-items a, 
.menu-items li {
    text-decoration: none;
    color: rgb(255, 230, 0);
    font-weight: bold;
}

.menu-items {
    position: absolute;
    top: 0;
    right: 0;
    height: 100vh;
    width: 70%;
    background-color: rgb(0, 0, 0);
    border: 1px solid rgb(0, 0, 0);
    display: flex;
    flex-direction: column;   /* stavke u kolonu */
    align-items: center;      /* centrirano */
    justify-content: flex-start;
    padding-top: 150px;       /* razmak od vrha */
    gap: 30px;                /* razmak između stavki */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 24px;
    list-style: none;
}


.border {
    border: 1px solid rgb(255, 230, 0);
    height: 100px;
    width: 50%;
    margin-left: 24%;
    border-radius: 20px;
    margin-top: 50px;
    position: fixed;
    display: flex;
    background-color: rgb(0, 0, 0);
    z-index: 99;
}

.logo {
    border-radius: 500px;
    height: 100px;
    margin-left: 80px;
}

.onama {
    color: white;
    margin-left: 380px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    text-decoration: none;
    
}

.cenovnik {
    color: white;
    margin-left: 60px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    text-decoration: none;
}

.slike {
    color: white;
    margin-left: 60px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    text-decoration: none;
}

.lokacija {
    color: white;
    margin-left: 60px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    text-decoration: none;
}

.kontakt {
    color: rgb(0, 0, 0);
    background-color: rgb(255, 230, 0);
    width: 140px;
    border-radius: 12px;
    height: 60px;
    font-size: 19px;
    font-weight: bold;
    border: none;
    margin-left: 60px;
    margin-top: 20px;
}
.lg {
    margin-left: 80px;
    margin-top: 50px;
}


@media (max-width: 1024px) {
    .border {
        width: 90%;
        margin-left: 5%;
        margin-top: 40px;
    }


    .logo {
        margin-left: 20px;
    }

    .onama,
    .cenovnik,
    .kontakt,
    .lokacija,
    .slike {
        display: none;
    }

    .menub {
        display: block;
        background: none;
        border: none;
        color: rgb(255, 230, 0);
        font-size: 40px;
        right: 5%;
        top: 25%;
        position: absolute;
    }
}

@media (min-width: 1025px) and (max-width: 1200px) {
    .border {
        width: 80%;
        margin-left: 10%;
    }
    .onama {
        margin-left: 40px;
    }
    .logo {
        margin-left: 20px;
    }
}
@media (min-width: 1201px) and (max-width: 1400px) {
    .border {
        width: 80%;
        margin-left: 10%;
    }
    .onama {
        margin-left: 140px;
    }
    .logo {
        margin-left: 50px;
    }
}
@media (min-width: 1401px) and (max-width: 1700px) {
    .border {
        width: 80%;
        margin-left: 10%;
    }
    .onama {
        margin-left: 280px;
    }
    .logo {
        margin-left: 50px;
    }
}
@media (min-width: 1701px) and (max-width: 2500px) {
    .border {
        width: 55%;
    }
    .onama {
        margin-left: 120px;
    }
    .logo {
        margin-left: 50px;
    }
}

</style>