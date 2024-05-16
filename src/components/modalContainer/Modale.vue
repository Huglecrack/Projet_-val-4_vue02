<template>
    <div class="modaleBackground01">

        <div class="overlay01"></div>

        <div class="contourFondImage01">
            <img src="@/assets/images/fermer.png" alt="fermer" class="fermer01">
            <img src="@/assets/images/CVfond.png" alt="CVfond" class="fondImage01">
        </div>

    </div>

    <div class="modaleBackground02">

        <div class="overlay02"></div>

        <div class="contourFondImage02">
            <img src="@/assets/images/fermer.png" alt="fermer" class="fermer02">
            <img src="@/assets/images/formulaireFond.png" alt="formulaireFond" class="fondImage02">
        </div>

    </div>

    <div class="modaleBackground03">

        <div class="overlay03"></div>

        <div class="modale03">
            <img src="../assets/images/fermer.png" class="fermer03">
            <h3>PortFolio d'HUGO Leplingard</h3>
            <p>dernière mise à jour le 02 avril 2024</p>
            <p>Ce site est fait de 92.2% de Vue, 3.4% d'HTML, 3.2% de JavaScript et de 1.2% de CSS</p>
            <a href="http://localhost:5175/" target="_blank">Cliquez pour voir le site</a><br>
            <a href="http://github.com/Huglecrack/Projet_-val-4_vue02.git" target="_blank" rel="noopener noreferrer">Liens vers le Repository Github</a>
        </div>
    </div>
</template>


<script>
    const clickModale1 = document.getElementById(modale1)
    const clickModale2 = document.getElementById(modale2)
    const clickModale3 = document.getElementById(modale3)

    clickModale1.addEventListener('click', function() {
        modaleBackground01.style.display = "block";
    });

    clickModale2.addEventListener('click', function() {
        modaleBackground02.style.display = "block";
    });

    clickModale3.addEventListener('click', function() {
        modaleBackground3.style.display = "block";
    });

    fermer01.addEventListener('click', function() {
        modaleBackground01.style.display = "none";
    });

    fermer02.addEventListener('click', function() {
        modaleBackground02.style.display = "none";
    });

    fermer03.addEventListener('click', function() {
        modaleBackground3.style.display = "none";
    });

</script>


<style scoped>
.modaleBackground01 {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
}

.overlay01 {
    position: fixed;
    background-color: rgb(0, 0, 0,0.7);
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.contourFondImage01 {
    display: flex;
    position: fixed;
    align-items: center;
    background-color: rgb(0, 0, 0);
    box-shadow: 0 0 100px 10px #2c269d;
    top: 0;
    bottom: 0;
    padding: 0 100px;
}

.fermer01 {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 30px;
    height: 30px;
    border-radius: 15%;
}

.fondImage01 {
    width: 90%;
    height: 70%;
}


.modaleBackground02 {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
}

.overlay02 {
    position: fixed;
    background-color: rgb(0, 0, 0,0.7);
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.contourFondImage02 {
    display: flex;
    position: fixed;
    align-items: center;
    background-color: rgb(0, 0, 0);
    box-shadow: 0 0 100px 10px #2c269d;
    top: 0;
    bottom: 0;
    padding: 0 100px;
}

.fermer02 {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 30px;
    height: 30px;
    border-radius: 15%;
}

.fondImage02 {
    width: 90%;
    height: 70%;
}


.modaleBackground03 {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 2;
}

.overlay03 {
    position: fixed;
    background-color: rgb(0, 0, 0,0.7);
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.modale03 {
    display: flex;
    position: fixed;
    left: 0;
    right: 0;
    padding: 60px 0;
    background-color: rgb(0, 0, 0);
    box-shadow: 0 0 100px 10px #2c269d;
    flex-direction: column;
    align-items: center;
}

.modale03 a {
    text-decoration: none;
    color: #b7b7ce;
    background-color: #3024b0;
    box-shadow: 0 0 3px 3px #2c269d;
    padding: 5px;
    border-radius: 4%;
}

.modale03 img {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 30px;
    height: 30px;
    border-radius: 15%;
}

.modale03 img:active {
    opacity: 0.3;
}
</style>