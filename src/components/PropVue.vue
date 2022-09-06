<template>
    <div>hello</div>
    <div :style="{fontSize:postsFontSize+'em'}">
        <!-- <ChildComponent 
        title1="你好" box="box"/> -->
        <ChildComponent  
        v-for="post in posts" 
        v-bind:key="post.id"
        v-bind:post="post"
        v-on:enlarge-text="postsFontSize+=$event"/>
        
        <!-- 上面的是监听器 -->
    </div>
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
                {id:1,title:'post1',},
                {id:2,title:'post2'},
                {id:3,title:'post3'},
                {id:4,title:'post4'}
            ],
            postsFontSize:1,
        }
    },
    components: { ChildComponent }
}
</script>

<style scoped>

</style>