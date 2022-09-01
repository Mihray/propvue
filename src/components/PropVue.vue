<template>
    <div>hello</div>
    <div :style="{fontSize:postsFontSize+'em'}">
        <ChildComponent 
        title1="你好" box="box" 
        v-for="post in posts" 
        v-bind:key="post.id"
        v-bind:post="post"
        v-on:enlarge-text="postsFontSize+=0.1"/></div>
  </template>

<script>
import ChildComponent from './ChildComponent.vue';

// import ChildComponent from '../src/components/ChildComponent.vue'

export default {
    //     components: {
    //         ChildComponent,
    //   },
    data() {
        return {
            posts:[
                {id:1,title:'heihei',},
                {id:2,title:'xixi'},
                {id:3,title:'kuku'}
            ],
            postsFontSize:1,
        }
    },
    components: { ChildComponent }
}
</script>

<style scoped>

</style>