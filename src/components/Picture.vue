<template>
    <img :src="avatar" :alt="descricao">
    <MudarImagem @mudar-imagem="trocarImagem" />
</template>
<script>
    import MudarImagem from './MudarImagem.vue';
    export default {
        name: 'Picture',
        components: {    
            MudarImagem
        },
        data(){
            return {
                avatar: "/img/avatar.png",
                descricao: "João Victor"
            }
        },
        methods: {
            trocarImagem(){                
                if (this.avatar == "/img/avatar2.png") {
                    this.avatar = "/img/avatar.png";
                } else {
                    this.avatar = "/img/avatar2.png";
                }
            }
        }
    }
</script>