<template lang="">
    
</template>

<script>
export default {
    data() {
        return {
            
        }
    },
    props:{
        title: {
            required: true,
            type: String,
        },
        content: {
            required: true,
            type: String,
        },
        image: {
            required: false,
            type: String,
        },
        linkRoute: {
            required: false,
            type: [ Object, String ]
        },
        linkLabel: {
            required: false,
            type: String,
        },
        fullLength: {
            required: false,
            type: Boolean,
        },
    }
}
</script>



<style lang="css"></style>