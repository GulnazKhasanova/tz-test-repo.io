<template>
<!--    <yandex-map-->
<!--      :coords="coords"-->
<!--      :zoom="10"-->
<!--      @click="onClick" :settings="settings"-->
<!--  >-->
<!--    <ymap-marker-->
<!--        :coords="coords"-->
<!--        marker-id="123"-->
<!--        hint-content="some hint"-->
<!--    />-->
<!--  </yandex-map>-->
    <yandex-map :coords="coords" :zoom="10" >
      <ymap-marker
          marker-id="123"
          :coords="coords"
          :icon="markerIcon"
      />
    </yandex-map>
</template>

<script>
 import { yandexMap, ymapMarker } from 'vue-yandex-maps'
export default {
  components: { yandexMap, ymapMarker},
  data(){
    return {
      coords: [
        54.82896654088406,
        39.831893822753904,
      ],
      markerIcon: {
        layout: 'default#imageWithContent',
        imageHref: 'https://image.flaticon.com/icons/png/512/33/33447.png',
        imageSize: [43, 43],
        imageOffset: [0, 0],
        content: '123 v12',
        contentOffset: [0, 15],
        contentLayout: '<div style="background: red; width: 50px; color: #FFFFFF; font-weight: bold;">$[properties.iconContent]</div>'
      }
    }
  },
  name: "mapcomponent"
}
</script>
<style lang="scss" scoped>
.ymap-container {
  height: 450px;
  margin: 176px auto;
  max-width: 1350px;
  min-height: 450px;
  width: 100%;
  border-radius: 50px;
}

</style>