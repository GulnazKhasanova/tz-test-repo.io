<template>
  <div class="map">
    <Mapcomponent></Mapcomponent>
  </div>
</template>

<script>
import Mapcomponent from "@/components/mapComponent/mapComponent";
export default {
name: "Maps",
  data(){
    return{}
  },
  components:{Mapcomponent}
}
</script>

<style lang="scss"  scoped>
.map{
  margin: 176px auto;
  max-width: 1350px;
  min-height: 450px;
  width: 100%;
  border-radius: 50px;
}

</style>