<template>
    <ChildComponent title='你好'/>{{title}}
</template>
<script>
    import { title } from 'process';
import ChildComponent from './components/ChildComponent.vue'
export default {
    components: {
        ChildComponent
  },
}
</script>
<style scoped>

</style>