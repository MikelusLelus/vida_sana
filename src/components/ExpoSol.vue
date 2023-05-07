
<template>
  <div>
    <div class="aplicacio">
      <div class="videoSol">
        <YouTubePlayer 
          videoUrl="https://www.youtube.com/embed/WDv4AWk0J3U" 
        />
      </div>
    </div>
    <div class="text_explicatiu">
    <p>
    Exposar-se a la llum solar durant uns 2-10 minuts cada matí mentre es camina a l'aire lliure és un hàbit que pot tenir efectes positius en el nostre benestar general. Aquesta pràctica ajuda a estimular la producció de cortisol, que ens ajuda a despertar i a tenir energia durant el dia, i també ajuda a iniciar la producció de melatonina, que és important per dormir bé a la nit. Si no es pot prendre sol, es pot fer servir una llum artificial en el seu lloc encara que no te el mateix efecte.
    </p>
    <p>
    A més a més, aquesta exposició diària a la llum solar ajuda a regular el cicle circadià, que és el rellotge intern del nostre cos que controla el ritme dels processos biològics. Això significa que prendre sol cada matí ajuda a sincronitzar el nostre rellotge intern i a mantenir un horari saludable per dormir, menjar i realitzar altres activitats importants.   
    </p>
    <p>
    En resum, l'hàbit d'exposició al sol pot tenir efectes positius en la nostra salut mental i física, i és una pràctica senzilla que tothom pot incorporar a la seva rutina matinal.
    </p>
    </div>
  </div>
</template>

<script>
import YouTubePlayer from './YouTubePlayer.vue';

  export default {
    name: 'ExpoSol',
    components: {
      YouTubePlayer,
    }
  }
</script>

<style>

.videoSol iframe {
  width: 70vw;
  height: 40vw;
}

</style>
