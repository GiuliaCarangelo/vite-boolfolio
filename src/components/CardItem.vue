<template lang="">
    <div>
        <div class="card" style="width: 18rem;">
            <img :v-if="image" :src="image" class="card-img-top mb-3" alt="img">
        <div class="card-body">
            <h1 class="card-title">{{ title }}</h1>
                <p class="card-text">{{ content }}</p>
        </div>
    </div>
</div>
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