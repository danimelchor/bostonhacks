<template>
  <div id="app">
      <DeckGL ref="deck"
            :class="['fill-wrapper']"
            :controlMap="true"
            :layers="layers"
            :width="'100%'"
            :height="'100%'"
            :controller="true"
            :useDevicePixels="false"
            :viewState="{latitude: 40, longitude: -100, zoom: 2.5, maxZoom: 10, pitch: 0, bearing: 0}"
            >
      <Mapbox class="fill-wrapper" 
                :accessToken="'pk.eyJ1IjoiZG1lbGNob3IiLCJhIjoiY2toaWJsNnhyMGEzbTJ6c2RmZWRzY3EyMiJ9.55wKLQ9Yze26jToMLOMQ2g'"                 
                :center="[-100,40]"
                :zoom="2.5"
                :bearing="0"
                :pitch="0"/>
    </DeckGL>
  </div>
</template>

<script>
import {DeckGL, Mapbox} from '@hirelofty/vue_deckgl'
import {ScreenGridLayer} from '@deck.gl/aggregation-layers';
import {isWebGL2} from '@luma.gl/core';


const colorRange = [/*
  [255, 255, 178, 25],*/
  [254, 217, 118, 85],
  [254, 178, 76, 127],
  [253, 141, 60, 170],
  [240, 59, 32, 212],
  [189, 0, 38, 255]
];

export default {
  name: 'Map',
  components: {
    DeckGL,
    Mapbox
  }, 
  data(){
      return{
          layers:[]
      }
  },
  mounted(){
        this.layers.push(new ScreenGridLayer({
            id: 'mylayer',
            data: 'https://raw.githubusercontent.com/danimelchor/bostonhacks/main/fastfood-dataset.json',
            opacity: 0.8,
            getPosition: d => [d[1], d[0]],
            getWeight: d => d[2],
            cellSizePixels: 10,
            colorRange,
            gpuAggregation: true,
            aggregation: 'SUM'
        }))
  }
}
</script>

<style lang="scss">
.fill-wrapper {
    position: absolute;
    width: 58vw;
    height: 30vw;
    left: 50%;
    transform: translateX(-50%);
    border-radius: 5px;
}

@media (max-width: 1200px) {
  .fill-wrapper {
      width: 100vw;
      height: 50vw;
      border-radius: 0;
  }
}

@media (max-width: 600px) {
  .fill-wrapper {
      width: 100vw;
      height: 100%;
      border-radius: 0;
  }
}
</style>