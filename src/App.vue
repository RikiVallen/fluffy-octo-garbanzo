
<template>
  <HelloWorld :tracks="tracks" />
</template>

<script setup lang="ts">
import { useLocalStorage } from '@vueuse/core';
import HelloWorld from './components/HelloWorld.vue'

interface Track {
	id: number,
	name: string,
	artist: string,
	album: string
}

const tracks = useLocalStorage<Track[]>('tracks', []);
</script>
