<template>
    <div>
      <iframe
        :src="videoUrl"
        allowfullscreen
      ></iframe>
    </div>
  </template>
  
<script>
  export default {
    name: "YouTubePlayer",
    props: {
      videoUrl: {
        type: String,
        required: true,
      },
    },
  }
</script>
  
  