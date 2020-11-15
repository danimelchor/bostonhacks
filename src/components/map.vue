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
            :viewState="{latitude: 40.73, longitude: -73.75, zoom: 9.6, maxZoom: 16, pitch: 0, bearing: 0}"
            >
      <Mapbox class="fill-wrapper" 
                :accessToken="'pk.eyJ1IjoiZG1lbGNob3IiLCJhIjoiY2toaWJsNnhyMGEzbTJ6c2RmZWRzY3EyMiJ9.55wKLQ9Yze26jToMLOMQ2g'"                 
                :center="[0,30]"
                :zoom="9.6"
                :bearing="0"
                :pitch="0"/>
    </DeckGL>
  </div>
</template>

<script>
import {DeckGL, Mapbox} from '@hirelofty/vue_deckgl'
import {ScreenGridLayer} from '@deck.gl/aggregation-layers';
import {isWebGL2} from '@luma.gl/core';


const colorRange = [
  [255, 255, 178, 25],
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
            data: 'https://raw.githubusercontent.com/visgl/deck.gl-data/master/examples/screen-grid/uber-pickup-locations.json',
            opacity: 0.8,
            getPosition: d => [d[0], d[1]],
            getWeight: d => d[2],
            cellSizePixels: 20,
            colorRange,
            gpuAggregation: true,
            aggregation: 'SUM'
        }))
  }
}
</script>

<style>
.fill-wrapper {
    position: absolute;
    width: 58vw;
    height: 30vw;
    left: 50%;
    transform: translateX(-50%);
}
</style>