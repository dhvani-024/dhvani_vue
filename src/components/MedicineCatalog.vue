<template>
  <div v-for="medicine of medicines" :key="medicine.code" >
    <IndividualMedicine :medicine=medicine />
  </div>
</template>


<script>
import IndividualMedicine from "./IndividualMedicine.vue";

export default{
    name:"MedicineCatalog",
    components:{
        IndividualMedicine
    },
    props:{
      medicines:Array
    }
}
</script>


<style>

</style>