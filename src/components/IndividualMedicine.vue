<template>
<div class="medicine_card">
<div class="medicine_photo">
    <img :src="medicine.medicine_image" alt="medicine_img" id="image"/>
</div>

<div class="medicine_details">
    <h2> Name: {{medicine.medicine_name}} </h2>
    <h3> Price: {{medicine.medicine_price}}</h3>
    <h4> Quantity: {{medicine.medicine_quantity}} </h4>
    <h4> In Stock: {{medicine.medicine_stock}} </h4>
    <h4> Expiry Date: {{medicine.medicine_expiryDate}} </h4>
</div>

</div>
</template>


<script>
export default{
    name:"IndividualMedicine",
    props:{
        medicine:Object
    }
}
</script>

<style>
    .medicine_card{
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        border:transparent;
        border-radius: 4px;
        padding: 10px;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
        width:80%;
        margin:auto;
        margin-bottom: 1em;
    }

    .medicine_photo #image{
        width: 250px;
        height: 250px;
    }
</style>