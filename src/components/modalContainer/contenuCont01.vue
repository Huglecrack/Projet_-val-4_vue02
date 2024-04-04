<template>
    <modalCont01 v-bind:reveleCont01="reveleCont01" v-bind:toggleModalCont01="toggleModalCont01"></modalCont01>
    <figure>
        <h2>Curiculum Vitae</h2>

        <div class="containerCont01" v-on:click="toggleModalCont01">
            <img src="@/assets/images/CVfond.png" alt="CVfond" class="fondImage01">

            <div class="middleCont01" v-on:click="toggleModalCont01">
                <img src="@/assets/images/cv.png" alt="logoCV">
            </div>
        </div>
    </figure>

</template>

<script>
    import ModalCont01 from './modalCont01.vue'

    export default {
        name: 'ContenuCont01',
        data (){
            return {
                reveleCont01: false
            }
        },
        components: {
            'modalCont01': ModalCont01
        },
        methods: {
            toggleModalCont01:function () {
                this.reveleCont01 = !this.reveleCont01
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

    .containerCont01 {
        margin-top: 10px;
        width: 400px;
        height: 500px;
        background-color: #080808;
    }

    .fondImage01 {
        width: 100%;
        height: 100%;
    }

    .containerCont01:hover .fondImage01 {
        transition: 1s ease;
        opacity: 0.3;
    }

    .containerCont01:hover .middleCont01 {
        opacity: 1;
        transition: 1s ease;
    }

    .containerCont01:hover + .headerCV {
        background-color: #080808;
    }

    .containerCont01:hover + .headerCV {
        background-color: #080808;
    }

    .containerCont01:hover + .cube {
        opacity: 1;
    }

    .middleCont01 {
        opacity: 0;
    }

    .middleCont01 img {
        position: absolute;
        top: 50%;
        left: 19%;
        width: 80px;
        height: 80px;
    }

    .middleCont01:hover {
        cursor: zoom-in;
    }

</style>