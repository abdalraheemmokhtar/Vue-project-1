


<template>
    <!-- <h1>This is a custome componet to learn how to make things work with vue</h1> -->
    <!-- <NewComp/> -->
    <FormComp/>
    <button class="new" @click="increment">click me {{ count }}</button>
    <button class="new" @click="togglecards">{{btnTxt}}</button>
    <div v-if="toggle"  class="cards">
    <CardComp title="Welcome to My Vue Card" content="This is a simple card component in Vue.js." />
    <CardComp title="Welcome to My Vue Card" content="This is a simple card component in Vue.js." />
    <CardComp title="Welcome to My Vue Card" content="This is a simple card component in Vue.js." />
    </div>

</template>

<script>

// import NewComp from './NewComp.vue';
import CardComp from './CardComp.vue'
import FormComp from './FormComp.vue'
export default {
    name: 'CustomComp',
    components: {  CardComp,FormComp }
}
</script>

<script setup>
import { ref } from 'vue'
const toggle = ref(true)
const btnTxt = ref('Hide Cards')
const count = ref(0)

function increment() {
  // update component state
  count.value++
}
function togglecards(){
    toggle.value = !toggle.value
    btnTxt.value = toggle.value?'Hide Cards':'Show Card'
}
</script>
<style scoped>
.cards{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  max-width: 1800px;
  margin: 0 auto;
}
.new{
    color:brown;
}
</style>