<template>
    <div class="modalContBackground02" v-if="reveleCont02">

        <div class="overlayCont02" v-on:click="toggleModalCont02"></div>

        <div class="contourFondImage02">
            <img src="@/assets/images/fermer.png" alt="fermerCont02" class="fermerCont02" v-on:click="toggleModalCont02">
            <img src="@/assets/images/formulaireFond.png" alt="formulaireFond" class="fondImage02">
        </div>

    </div>

</template>


<script>

    export default {
        name: 'ModalCont02',
        props: ['reveleCont02', 'toggleModalCont02']
    }

</script>



<style scoped>

    .modalContBackground02 {
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

    .overlayCont02 {
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

    .fermerCont02 {
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

</style>
