<template>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} e a minha profissão é {{profissao}}</p>
    <MultiplosEventos />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
</template>

<script>

    import MultiplosEventos from './MultiplosEventos.vue';
    import Reutilizacao from './Reutilizacao.vue';

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return {
                nome: "Matheus",
                profissao: "Programador"
            }    
        }
    }
</script>