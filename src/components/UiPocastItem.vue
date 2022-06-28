<script lang="ts" setup>
interface UiPodcastProps {
  thumbnail: string
  slug: string
}
const props = defineProps<UiPodcastProps>()
// const name = $ref(user.savedName)
const router = useRouter()
const onPodcastItemClicked = (slug: string) => router.push(`/episode/${slug}`)
</script>

<template>
  <article class="rounded-lg overflow-hidden relative cursor-pointer shadow overlayed">
    <div class="absolute w-full h-full transition-all overlay" @click="onPodcastItemClicked(props.slug)" />
    <img :src="props.thumbnail" :alt="props.slug">
  </article>
</template>

<style scoped>
.overlayed:hover > .overlay {
  background-color: rgba(0, 0, 0, 0.5);
}
</style>
