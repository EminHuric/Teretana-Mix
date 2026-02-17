<template>
    <div class="border">
        <img alt="logo" src="/logo.png" class="logo">
        <p class="onama">O nama</p>
        <p class="cenovnik">Cenovnik</p>
        <p class="slike">Slike</p>
        <p class="lokacija">Lokacija</p>
        <button class="kontakt">Kontakt</button>
    </div>
    
</template>

<style scoped>
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
}
.cenovnik {
    color: white;
    margin-left: 60px;
     margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
}
.slike {
    color: white;
    margin-left: 60px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
}
.lokacija {
    color: white;
    margin-left: 60px;
    margin-top: 40px;
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
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
@media (max-width: 480px) {
    .border {
        width: 87%;
        margin-left: 5%;
        margin-top: 40px;
    }
}
</style>