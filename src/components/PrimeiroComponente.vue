<template>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} e a minha profissão é {{profissao}}</p>
    <MultiplosEventos />
</template>

<script>

    import MultiplosEventos from './MultiplosEventos.vue';

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos
        },
        data(){
            return {
                nome: "Matheus",
                profissao: "Programador"
            }    
        }
    }
</script>