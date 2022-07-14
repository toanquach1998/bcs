<template>
  <q-card class="bg-transparent no-shadow no-border">
    <q-card-section class="q-pa-none">
      <div class="row q-col-gutter-sm ">
        <div class="col-lg-4 col-md-4 col-xs-12 col-sm-12">

        </div>
        <div class="col-lg-4 col-md-4 col-xs-12 col-sm-12">

          <div class="col-lg-4 col-md-4 col-xs-12 col-sm-12" color="red"></div>
          
          <div class="col-lg-4 col-md-4 col-xs-12 col-sm-12"></div>>
        </div>
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: "cardsocial",
  
        setup () {
      return {
          test1[
          {
            title: "Monthly Income",
            icon: "fas fa-dollar-sign",
            value: "$ 20k",
            color1: "#546bfa",
          },
          {
            title: "Weekly Sales",
            icon: "fas fa-chart-bar",
            value: "20",
            color1: "#3a9688",
          },
          {
            title: "New Customers",
            icon: "fas fa-chart-line",
            value: "321",
            color1: "#7cb342",
          },
          {
            title: "Active Users",
            icon: "person",
            value: "82",
            color1: "#f88c2b",
          
      } ]
   }
  }
})
</script>

<style>

.card-social{
  border-radius: 10px;
  padding: 5px 0 0 5px;
  margin: 0 10px 0 10px;

}

</style>