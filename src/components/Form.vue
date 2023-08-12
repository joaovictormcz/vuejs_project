<template>
    <div>
        <form action="">
            <h2>Meu formulário</h2>
            <div>
                <InputText />
            </div>
            <div>
                <InputText />
            </div>
            <div>
                <Submit />
            </div>
        </form>
    </div>
</template>

<script>
    import InputText from './form/InputText.vue';
    import Submit from './form/Submit.vue'
    
    export default {
        name: 'Form',
        components: {
            InputText,
            Submit
        }
    }
</script>