<template>
        <input data-index="Index" ref="`${'input-'}${Index}" type="text"  @input="focusNextOncePopulated($event, 1)" v-model="message"/>

</template>

<script>
export default{
    name:"Smallletterbox"
}
</script>

<style>

</style>