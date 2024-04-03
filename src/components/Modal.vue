<template>
    <div class="modalBackground" v-if="revele">

        <div class="overlay" v-on:click="toggleModal"></div>

        <div class="modal">
            <img src="../assets/images/fermer.png" v-on:click="toggleModal">
            <h3>Porte-Folio d'HUGO Leplingard</h3>
            <p>ernière mise à jour le 02 avril 2024</p>
            <p>Ce site est fait de 88.9% de Vue, 4.8% de JavaScript, 4.5% d'HTML et de 1.8% de CSS</p>
            <a href="http://localhost:5175/" target="_blank">Cliquez pour voir le site</a><br>
            <a href="http://github.com/Huglecrack/Projet_-val-4_vue02.git" target="_blank" rel="noopener noreferrer">Liens vers le Repository Github</a>
        </div>
    </div>
</template>



<script>

    export default {
        name: 'Modal',
        props: ['revele', 'toggleModal']
    }

</script>



<style scoped>

.modalBackground{
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

.overlay {
    position: fixed;
    background-color: rgb(0, 0, 0,0.7);
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.modal {
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

.modal a {
    text-decoration: none;
    color: #b7b7ce;
    background-color: #3024b0;
    box-shadow: 0 0 3px 3px #2c269d;
    padding: 5px;
    border-radius: 4%;
}

.modal img {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 30px;
    height: 30px;
    border-radius: 15%;
}

.modal img:active {
    opacity: 0.3;
}
</style>