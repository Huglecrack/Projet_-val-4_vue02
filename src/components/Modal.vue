
<template>
    <div class="modal">
        <div class="fermerModalDiv">
            <button class="envoieModal"><img src="../images/fermer.png"></button>
        </div>
        <h3>Porte-Folio d'HUGO Leplingard</h3>
        <p>crée le Mercredi 6 mars 2024</p>
        <p>Ce site est fait de 48.1% d'HTML, 42.7% de CSS et 9.2% de JavaScript</p>
        <a href="../assets/images/formulaire-de-contact.png">Cliquez pour voir le site</a><br>
        <a href="https://github.com/Huglecrack/Projet_-val-4_vue02.git">Liens vers le Repository Github</a>
    </div>
</template>



<script setup>

</script>



<style scoped>
.modal {
    width: 100%;
    height: 45%;
    display: flex;
    z-index: 1;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    border-top:solid 4px #2c269d;
    flex-direction: column;
    align-items: center;
    background-color: #2d2d2d;
}

.modal a {
    text-decoration: none;
    color: #b7b7ce;
    background-color: #3024b0;
    padding: 5px;
    border-radius: 20%;
}

.fermerModalDiv {
    width: 100%;
    margin-top: 15px;
    display: flex;
    justify-content: end;
}

.envoieModal,.envoieModal img {
    display: flex;
    width: 30px;
    height: 30px;
    margin-right: 15px;
    border-radius: 15%;
    background-color: #3024b0;
    justify-content: center;
    align-items: center;
}
</style>