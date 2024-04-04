<template>
    <modalPrés v-bind:revelePrés="revelePrés" v-bind:toggleModalPrés="toggleModalPrés"></modalPrés>
    <div v-on:click="toggleModalPrés"> 
        <button>Appuyez pour ouvrir le Modal</button>
    </div>
</template>



<script>
    import ModalPrés from './ModalPrés.vue'

    export default {
        name: 'ContenuPrés',
        data (){
            return {
                revelePrés: false
            }
        },
        components: {
            'modalPrés': ModalPrés
        },
        methods: {
            toggleModalPrés:function () {
                this.revelePrés = !this.revelePrés
            }
        }
    }
</script>



<style scoped>
    div {
        right: 0;
        left: 0;
        margin-top: 150px;
        display: flex;
        justify-content: center;
    }

    div button {
        font-family: 'Lato', sans-serif;
        background-color: #3024b0;
        color: #b7b7ce;
        font-size: 15px;
        padding: 15px 25px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }
</style>