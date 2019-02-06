<template>
  <div class="col-md-8" v-if="video">
    <div class="details">
      <div class="embed-responsive embed-responsive-16by9">
        <iframe
          class="embed-responsive-item"
          :src="`https://www.youtube.com/embed/${video.id.videoId}`"
          allowfullscreen>
        </iframe>
      </div>
      <h4>{{ video.snippet.title }}</h4>
      <p>{{ video.snippet.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoDetail',
  props: {
    video: Object
  }
}
</script>

<style scoped>
.details {
  margin: 15px 0;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
}
</style>
