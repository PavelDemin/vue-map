<template>
	<div class="ya-wrap">
		<div class="ya-map">
			<h1>Рыболовная карта</h1>
			<yandex-map 
			  :coords="[48.480223, 135.071917]"
			  :zoom="zoom"
			  style="width: 800px; height: 600px;"
			  :cluster-options="{
			    1: {clusterDisableClickZoom: true}
			  }"
			  :behaviors="['multiTouch','scrollZoom','drag']"
			  :controls="['fullscreenControl','typeSelector','zoomControl']"
			  :placemarks="placemarks" 
			  map-type="map"
			>
 			</yandex-map>
		</div>
	</div>	
</template>

<script>
	import { yandexMap, ymapMarker } from 'vue-yandex-maps'
	import {yadata} from '../data.js'
		
	export default {
		name: 'YaMap',
		components: {
			yandexMap,
		  ymapMarker
		},
		props: {
			zoom: {
				type: Number,
				default: 8
			}
		},
		data() {
		  return {
		    placemarks: yadata
		  }
		}
	}
</script>

<style>
	.ya-wrap {
		width: 100%;
	}
	.ya-map {
		width: 800px;
		margin: 0 auto;
		text-align: center;
	}
</style>