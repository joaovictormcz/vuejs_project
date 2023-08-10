<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <p>Estou trabalhando no momento</p>
        <p>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>Java</li>
            <li>Python</li>
            <li>javaScript</li>
        </ul>
    </div>        
</template>
<script>
    export default {
        name: 'Pessoa',
        data(){
            return {
                nome: "João Victor"
            }
        }
    }
</script>