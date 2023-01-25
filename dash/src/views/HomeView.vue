<template>
  <div class="container animated zoomInUp">
    <ContainerBlock>
    </ContainerBlock>
  </div>
</template>

<script>
// @ is an alias to /src
import ContainerBlock from "@/components/ContainerBlock.vue";

export default {
  name: 'HomeView',
  components: {
    ContainerBlock,
  }
}
</script>

<style scoped>
body {
  background-color: black!important;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
</style>