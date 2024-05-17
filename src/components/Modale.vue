<template>

    <div class="modaleBackground01" v-if="reveleModale01">
        <div class="overlay01" v-on:click="toggleModale01"></div>

        <div class="modale01">
            <img src="@/assets/images/fermer.png" alt="fermer" class="fermer01" v-on:click="toggleModale01">
            <img src="@/assets/images/CVfond.png" alt="CVfond" class="fondImage01">
        </div>
    </div>

    <div class="modaleBackground02" v-if="reveleModale02">
        <div class="overlay02" v-on:click="toggleModale02"></div>

        <div class="modale02">
            <img src="@/assets/images/fermer.png" alt="fermer" class="fermer02" v-on:click="toggleModale02">
            <img src="@/assets/images/formulaireFond.png" alt="formulaireFond" class="fondImage02">
        </div>
    </div>

    <div class="modaleBackground03" v-if="reveleModale03">
        <div class="overlay03" v-on:click="toggleModale03"></div>

        <div class="modale03">
            <img src="../assets/images/fermer.png" class="fermer03" v-on:click="toggleModale03">
            <h3>PortFolio d'HUGO Leplingard</h3>
            <p>dernière mise à jour le 02 avril 2024</p>
            <p>Ce site est fait de 92.2% de Vue, 3.4% d'HTML, 3.2% de JavaScript et de 1.2% de CSS</p>
            <a href="http://localhost:5175/" target="_blank">Cliquez pour voir le site</a><br>
            <a href="http://github.com/Huglecrack/Projet_-val-4_vue02.git" target="_blank" rel="noopener noreferrer">Liens vers le Repository Github</a>
        </div>
    </div>

</template>


<script>

    export default {
        name: 'Modale',
        props: ['reveleModale01', 'reveleModale02', 'reveleModale03', 'toggleModale01', 'toggleModale02', 'toggleModale03']
    }

</script>


<style scoped>

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