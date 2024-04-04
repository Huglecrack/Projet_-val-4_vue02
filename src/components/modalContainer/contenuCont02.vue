<template>
    <modalCont02 v-bind:reveleCont02="reveleCont02" v-bind:toggleModalCont02="toggleModalCont02"></modalCont02>
    <figure>
        <h2>Formulaire</h2>

        <div class="containerCont02" v-on:click="toggleModalCont02">
            <img src="@/assets/images/formulaireFond.png" alt="formulaireFond" class="fondImage02">

            <div class="middleCont02">
                <img src="@/assets/images/formulaire-de-contact.png" alt="logoFormulaire">
            </div>
        </div>
    </figure>

</template>

<script>
    import ModalCont02 from './modalCont02.vue'

    export default {
        name: 'ContenuCont02',
        data (){
            return {
                reveleCont02: false
            }
        },
        components: {
            'modalCont02': ModalCont02
        },
        methods: {
            toggleModalCont02:function () {
                this.reveleCont02 = !this.reveleCont02
            }
        }
    }
</script>

<style scoped>

    figure {
        margin-top: 50px;
    }

    figure h2 {
       padding-left: 110px;
    }

    .containerCont02 {
        margin-top: 10px;
        width: 400px;
        height: 500px;
        background-color: #080808;
    }

    .fondImage02 {
        width: 100%;
        height: 100%;
    }

    .containerCont02:hover .fondImage02 {
        transition: 1s ease;
        opacity: 0.3;
    }

    .containerCont02:hover .middleCont02 {
        opacity: 1;
        transition: 1s ease;
    }

    .containerCont02:hover + .headerFDC {
        background-color: #080808;
    }

    .containerCont02:hover + .headerFDC {
        background-color: #080808;
    }

    .containerCont02:hover + .cube {
        opacity: 1;
    }

    .middleCont02 {
        opacity: 0;
    }

    .middleCont02 img {
        position: absolute;
        top: 50%;
        left: 54%;
        width: 80px;
        height: 80px;
    }

    .middleCont02:hover {
        cursor: zoom-in;
    }

</style>