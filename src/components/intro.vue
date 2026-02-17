<template>
    <section class="hero">
        <!-- Video pozadina -->
        <video autoplay muted loop class="hero-video">
            <source src="/video.mp4" type="video/mp4" />
            Your browser does not support the video tag.
        </video>

        <div class="overlay">
            <h2 class="em">Teretana MIX Prijepolje</h2>
            <h2 class="e">Budi Najjača Verzija Sebe</h2>
            <p class="p">Pridruži se i treniraj u prostoru koji podstiče napredak, snagu i kondiciju.</p>
            <div class="container">
                <button>Zakaži probni trening</button>
                <button>Kako doći do nas?</button>
            </div>
            <div class="statistic">
                <i class="fa-sharp fa-solid fa-people-group"></i>
                <span>5000+</span> zadovoljnih članova
            </div>

        </div>
    </section>
</template>

<script setup>
const bookTrial = () => {
    alert("Hvala! Kontaktiraćemo te za probni trening.");
}
</script>

<style scoped>
.statistic {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 2rem;
    font-weight: bold;
    color: #FFD700;
    margin-bottom: 20px;
    margin-top: 50px;
}

.statistic i {
    font-size: 2.5rem;
    color: #FFD700;
}

.em {
    font-size: 100px;
    color: #FFD700;
}

.e {
    font-size: 70px;
    color: #ffffff;
    margin-top: -70px;
}

.hero {
    position: relative;
    height: 100vh;
    width: 100vw;
    overflow: hidden;
    z-index: 1;
}

.hero-video {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 0;
}

.overlay {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    text-align: center;
    padding: 50px;
    color: white;

    /* manje mutan overlay */
    background-color: rgba(0, 0, 0, 0.5);
    text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.6);
}



.p {
    font-size: 24px;
    margin-bottom: 20px;
    margin-top: -10px;
}

button,
.maps-button {
    padding: 12px 25px;
    font-size: 1.1rem;
    border-radius: 5px;
    font-weight: bold;
    margin: 10px;
}

button {
    background-color: #FFD700;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #e6c200;
}

.maps-button {
    color: black;
    background-color: #FFD700;
    text-decoration: none;
}

.maps-button:hover {
    background-color: #e6c200;
}

/* Mobilni uređaji: 0px - 768px */
@media (min-width: 0px) and (max-width: 768px) {
    .em {
        margin-top: 140px;
        font-size: 50px;
        width: 110%;
    }
    .e {
        margin-top: -25px;
        font-size: 40px;
        width: 101%;
    }
    .p {
        font-size: 20px;
    }
    .statistic {
        margin-top: 20px;
        font-size: 18px;
        z-index: 999;
    }
}

/* Tableti: 769px - 1024px */
@media (min-width: 769px) and (max-width: 1024px) {
    .em {
        margin-top: 80px;
        font-size: 65px;
        width: 110%;
    }
    .e {
        margin-top: -30px;
        font-size: 55px;
        width: 101%;
    }
    .p {
        font-size: 22px;
    }
    .statistic {
        margin-top: 20px;
        font-size: 18px;
        z-index: 999;
    }
}


@media (min-width: 1025px) and (max-width: 1400px) {
    .em {
        font-size: 90px;
        margin-top: 50px;
    }
}
@media (min-width: 1401px) and (max-width: 50000px) {
    .em {
        font-size: 90px;
        margin-top: 50px;
    }
}
</style>
