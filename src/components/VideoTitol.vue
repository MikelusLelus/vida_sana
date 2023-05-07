<template>
    <div>
      <div class="videoMida">
        <YouTubePlayer 
          :videoUrl="newVideoUrl"
        />
    </div>  
      <div class="titol-boto">
       <span class="estil_titol">{{ videoTitle }} </span> 
    </div>
    </div>
</template>
  
  <script>
import YouTubePlayer from './YouTubePlayer.vue';
  
  export default {
    name: 'VideoTitol',
    components: {
        YouTubePlayer,
    },
    props: {
      videoTitle: {
        type: String,
        required: true,
      },
      newVideoUrl: {
        type: String,
        required: true,
      },
    },
  };
  </script>

<style>
.estil_titol{
        font-family: 'Roboto', sans-serif;
        font-weight: 500;
        font-size: 18px;
        background-color: white;
        color: #1565C0;
        padding: 10px 40px;
        border: 1px solid black;
        border-radius: 20px;

}

.videoMida {
    padding: 15px;
   
}

.videoMida iframe {
    width: 25vw;
    height: 15vw;
}

</style>