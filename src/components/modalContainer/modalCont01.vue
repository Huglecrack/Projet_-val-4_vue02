<template>
    <div class="modalContBackground01" v-if="reveleCont01">

        <div class="overlayCont01" v-on:click="toggleModalCont01"></div>

        <div class="contourFondImage01">
            <img src="@/assets/images/fermer.png" alt="fermerCont01" class="fermerCont01"v-on:click="toggleModalCont01">
            <img src="@/assets/images/CVfond.png" alt="CVfond" class="fondImage01">
        </div>

    </div>

</template>


<script>

    export default {
        name: 'ModalCont01',
        props: ['reveleCont01', 'toggleModalCont01']
    }

</script>



<style scoped>

    .modalContBackground01 {
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

    .overlayCont01 {
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

    .fermerCont01 {
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

</style>