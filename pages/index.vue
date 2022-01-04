<template>
  <div id="loading"/>
</template>

<script>
export default {
  mounted() {
    setTimeout(() => {
     this.$router.push("/neofetch")
    }, 2000)
  }
}


</script>

<style>
#loading {
  background-color: black;

  width: 100vw;
  height: 100vh;
}

</style>
