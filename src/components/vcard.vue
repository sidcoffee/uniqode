<template>
<div :class="containerback">
    <h1>{{firstName}} {{lastName}}</h1>
    <h3>Email: <a :href="`${'mailto:'}${email}`">{{email}}</a></h3>
    <h3>Mobile: <a :href="`${'tel:'}${mobile}`">{{mobile}}</a></h3>
    <h1 v-if="mobile==`not given`">not</h1>

</div>
</template>
<script>
export default{
    name: "Vcard",
    props:{
        firstName:String,
        lastName:String,
        email: String,
        mobile: {
            type:String,
            default:"not given",
        },
        containerback:String,
    }
}
</script>

<style scoped>
.def{
    width:250px;
    padding:10px;
    border:1px solid #ccc;
    border-radius:5px;
}
.back{
    width:250px;
    padding:10px;
    border:1px solid #ccc;
    border-radius:5px;
    /* background-color: rgb(209, 39, 47); */
    display:none;
}
</style>