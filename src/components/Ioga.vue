<template>
  <div>
    <div class="aplicacio">
      <div class="columnes">
      <VideoTitol
            v-for="(ioga, index) in ioga_tipus"
            :key="index"
            :videoTitle="ioga.titol"
            :newVideoUrl="ioga.url"
          />
        </div>
    </div>
    <div class="text_explicatiu">
    <p>
    Practicar ioga te nombrosos beneficis per a la salut mental i física. A través de la combinació de postures, respiració i meditació, el ioga ajuda a millorar la flexibilitat, l'equilibri, la força i la concentració. També ajuda a reduir l'estrès, l'ansietat i la depressió. El ioga és una activitat accessible per a tothom, independentment de la edat o condició física. Pot ser tant una activitat solitària com grupal i es pot adaptar a les necessitats individuals de cadascú.
    </p>
    </div>
  </div>
</template>

<script>
 import VideoTitol from './VideoTitol.vue';

  export default {
    name: 'Ioga',
     components: {
        VideoTitol,
      },
      data () {
        return {
          ioga_tipus: [
          {
            url: 'https://www.youtube.com/embed/WamU36hXiNw',
            titol: 'Primera Clase'
          },
          {
            url: 'https://www.youtube.com/embed/p81lnqtkZcA',
            titol: 'Despertar'
          },
          {
            url: 'https://www.youtube.com/embed/QCNWDWx4n6k',
            titol: 'Flexibilitat'
          },
          {
            url: 'https://www.youtube.com/embed/bN_BD8YutjA',
            titol: 'Clase Express'
          },
          {
            url: 'https://www.youtube.com/embed/ORZqGpZguD0',
            titol: 'Clase Completa'
          },
          {
            url: 'https://www.youtube.com/embed/mPp0gvCsndA',
            titol: 'Activar el cos'
          },
          ]
        }
      }
  }
</script>