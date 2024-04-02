
<template>
    <div class="modalBackground" id="fermer">

        <div class="overlay"></div>

        <div class="modal">
            <img src="../assets/images/fermer.png" class="envoieModal">
            <h3>Porte-Folio d'HUGO Leplingard</h3>
            <p>crée le Mercredi 6 mars 2024</p>
            <p>Ce site est fait de 48.1% d'HTML, 42.7% de CSS et 9.2% de JavaScript</p>
            <a href="../assets/images/formulaire-de-contact.png">Cliquez pour voir le site</a><br>
            <a href="https://github.com/Huglecrack/Projet_-val-4_vue02.git">Liens vers le Repository Github</a>
        </div>
    </div>
</template>



<script>


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
    padding: 20px;
    background-color: rgb(0, 0, 0);
    box-shadow: 0 0 100px 30px #2c269d;
    flex-direction: column;
    align-items: center;
}

.modal a {
    text-decoration: none;
    color: #b7b7ce;
    background-color: #3024b0;
    box-shadow: 0 0 5px 3px #2c269d;
    padding: 5px;
    border-radius: 10%;
}

.envoieModal {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 30px;
    height: 30px;
    border-radius: 15%;
}

.envoieModal:active {
    opacity: 0.3;
}
</style>