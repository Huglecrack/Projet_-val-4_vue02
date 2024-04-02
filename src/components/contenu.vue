<template>
    <modal v-bind:revele="revele" v-bind:toggleModal="toggleModal"></modal>
    <div v-on:click="toggleModal"> 
        <button>Appuyez pour ouvrir le Modal</button>
    </div>
</template>



<script>
    import Modal from './Modal.vue'

    export default {
        name: 'Contenu',
        data (){
            return {
                revele: false
            }
        },
        components: {
            'modal': Modal
        },
        methods: {
            toggleModal:function () {
                this.revele = !this.revele
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