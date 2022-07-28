<template>
  <div>
    <nav class="navbar navbar-dark bg-primary rounded p-2">
      <div class="navbar-brand m-1" href="#">
        <span> {{titleNavbar}} </span>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'AMNavbar',
  props: {
    titleNavbar: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>



