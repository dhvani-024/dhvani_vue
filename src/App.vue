<template>
  <MedicineHeader/>
  <MedicineCatalog :medicines=medicines />
</template>

<script>
import MedicineCatalog from "./components/MedicineCatalog.vue";
import MedicineHeader from "./components/MedicineHeader.vue";

export default{
  name: "App",
  components:{
    MedicineCatalog,
    MedicineHeader
  },data(){
    return {
      medicines: []
    }
  },
  methods:{
    //promoises
    async fetchMedicines(){
      const res = await fetch('https://chemists.onrender.com/api');
      const data = await res.json()
      console.log(data[0].medicines);
      return data[0].medicines;
    }
  },
  async created(){
      this.medicines = await this.fetchMedicines();
  }
}
</script>

<style>

</style>