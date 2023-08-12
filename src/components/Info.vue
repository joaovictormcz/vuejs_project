<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li> 
            <li>Java</li>
            <li>Python</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBtn }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar o meu portfólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>   
        <Picture />
    </div>
</template>

<script>
    import Picture from './Picture.vue';
    export default {        
        name: 'Info',
        components: {
            Picture
        },
        data(){
            return {
                esta_trabalhando: true,
                mostrar_email: false,
                email: 'joaovictor.mcz@gmail.com',
                meu_link: 'https://google.com',
                textoBtn: 'Mostrar e-mail'
            }
        },
        methods:{
            showEmail(){
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.textoBtn = 'Mostrar e-mail'    
                } else {
                    this.textoBtn = 'Ocultar e-mail'
                }
            }
        }
    }
</script>