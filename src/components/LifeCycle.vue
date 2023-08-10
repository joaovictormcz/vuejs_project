<template>
    <div>
        <h1>Meu nome é: {{ nome }}</h1>
    </div>    
</template>

<script>
    export default {
        name: "LifeCycle",
        data(){
            return {
                nome: 'Ainda não sei'
            }
        },
        created(){
            this.nome = "Matheus"
        },
        mounted(){
            this.nome = "João Victor"
        }
    }
</script>