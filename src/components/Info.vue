<template>
    <div>
        <p>{{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnologias para Backend:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
                {{ technology }} 
            </li>             
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id"> 
                {{ technology.language }} 
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBtn }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar o meu portfólio basta <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>   
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
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data(){
            return {                
                mostrar_email: false,
                meu_link: 'https://google.com',
                textoBtn: 'Mostrar e-mail',
                backend_technologies: ["JavaScript", "Java", "Python", "Go"],
                frontend_technologies: [
                    {id: 1, language: 'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: 'Vue'}
                ]
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

<style>
    .paragrafo-pai {
        color: red;
    }
</style>