<template>
	<div v-for="track in tracks" :key="track.id"></div>
</template>

<script lang="ts" setup>
interface Track {
	id: number,
	name: string,
	artist: string,
	album: string
}

defineProps<{
	tracks: Track
}>()
</script>