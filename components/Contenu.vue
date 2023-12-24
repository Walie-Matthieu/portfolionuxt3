<template>
    <div class="parent">
        <Presentation/>
        <Page2/>
    </div>
</template>

<style scoped>
.parent {
    background-color: rgb(19, 10, 10);
    height: 100%;
    width: 100%;
    max-width: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>

<script>
import Presentation from './Presentation.vue';
import Page2 from './Page2.vue'

export default{
    components :{
        Presentation,
        Page2
    }
}
</script>
