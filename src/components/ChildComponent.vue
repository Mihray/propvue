<template>
    <div> 
        <h3>{{title1}}</h3>
        <h3>wowow--{{box}}</h3>
        <h3>{{post.title}}</h3>
        <button v-on:click="$emit('enlarge-text')">
            Enlarge text
        </button>
        
    </div>
</template>
<script>
export default {
    data(){

    },
    props:['title1','box','post'],
}
</script>
<style scoped>

</style>