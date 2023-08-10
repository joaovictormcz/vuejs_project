<template>
    <form action="">
        <div>
            <inputText/>
        </div>
        <div>
            <inputText/>
        </div>
        <div>
            <Submit/>
        </div>            
    </form>
</template>

<script lang="ts">
    import inputText from './form/inputText.vue'
    import Submit from './form/Submit.vue'
    
    export default {
        name: 'Form',
        components: {
            inputText,
            Submit
        }
    }
</script>