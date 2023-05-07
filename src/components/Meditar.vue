
<template>
    <div>
      <div class="aplicacio">
      <Temporitzador 
      :minuts="10"
      :audio-src="musica" />
      </div>
      <div class="text_explicatiu">
      <p>
        La meditació és una pràctica que implica centrar la ment en un objecte o pensament, amb l'objectiu de calmar la ment i reduir l'estrès i l'ansietat. Hi ha molts tipus diferents de meditació, incloent la meditació guiada, la meditació amb mantras i la meditació mindfulness. 
      </p>
      <p>
        Ajuda a millorar la concentració, la claredat mental i la capacitat per afrontar situacions estressants. A més, es una activitat fàcil de practicar en qualsevol lloc i moment, i no requereix equipament especial ni una gran quantitat de temps. 
      </p>
      </div>
    </div>
  </template>
  
  <script>
  import Temporitzador from './Temporitzador.vue';
  import musicaMeditar from '../assets/meditar.mp3' 

    export default {
      name: 'Meditar',
      components: {
        Temporitzador,
     },
     data () {
      return {
        musica: musicaMeditar,
      }
     }
    }
  </script>
