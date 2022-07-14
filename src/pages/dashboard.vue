<template>
  <cardSocial id="card-social"></cardSocial>
  <chartColumn></chartColumn>
  <chartPie></chartPie>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue';


const chartColumn = defineAsyncComponent(() =>
import('components/charts/columnchart.vue')
);

const cardSocial = defineAsyncComponent(()=>
import('components/cards/cardsocial.vue'));

const chartPie = defineAsyncComponent(()=>
import('components/charts/piechart.vue'));

export default defineComponent({
  name: 'dashboard',
 components: { 
    chartColumn,
    cardSocial, 
    chartPie,
 }

})
</script>

<style scoped>
#card-social{
    padding-top: 20px;
    padding-bottom: 20px;

}
</style>