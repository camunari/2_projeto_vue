<template>
  <img :src="avatar" :alt="descricao" width="200">
</template>

<script>
export default {
    name: 'Picture',
    data() {
        return {
        avatar: "/img/logo.png",
        descricao: "Carla Munari"
        }
    }
}
</script>

<style>

</style>