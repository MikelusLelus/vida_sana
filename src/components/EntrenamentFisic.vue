
<template>
    <div>
      <div class="aplicacio">
        <div class="columnes">
          <VideoTitol
            v-for="(entrenament, index) in entrenaments"
            :key="index"
            :videoTitle="entrenament.titol"
            :newVideoUrl="entrenament.url"
          />
        </div>
      </div>
      <div class="text_explicatiu">
      <p>
       L'entrenament físic és una part important per mantenir una vida saludable. A més de mantenir el cos en forma i saludable, també té beneficis per al benestar mental. L'activitat física ajuda a reduir l'estrès, millorar l'estat d'ànim i augmentar l'energia.
      </p>
      <p>
        Per obtenir els beneficis de l'entrenament físic, és important crear una rutina d'exercici regular. Això pot incloure una combinació d'exercicis de força, com peses o flexions, i exercicis aeròbics, com córrer o caminar. També és important permetre al cos temps de descans per recuperar-se i evitar lesions.
      </p>
      <p>
        Com amb qualsevol activitat física, és important començar amb una intensitat adequada i progressar lentament. Si tens alguna preocupació sobre la teva salut o si estàs començant una nova rutina d'exercici, és important parlar amb un professional de la salut abans de començar. Amb una planificació adequada i una rutina d'exercici regular, pots gaudir dels beneficis de l'entrenament físic durant tota la vida.
      </p>
      </div>
    </div>
  </template>
  
  <script>
  import VideoTitol from './VideoTitol.vue';

    export default {
      name: 'EntrenamentFisic',
      components: {
        VideoTitol,
      },
      data () {
        return {
          entrenaments: [
          {
            url: 'https://www.youtube.com/embed/wppLAEXbtOs',
            titol: 'Sense Equipament'
          },
          {
            url: 'https://www.youtube.com/embed/GY1JhB9BEkk',
            titol: 'Mancuernas'
          },
          {
            url: 'https://www.youtube.com/embed/lDJgpxoBQME',
            titol: 'TRX'
          },
          ]
        }
      }
    }
  </script>
<style>

</style>