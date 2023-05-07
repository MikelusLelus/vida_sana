<template>
     <OpcionsHabits
          v-for="(habit, index) in habits"
          :key="index"
          :foto="habit.foto"
          :text="habit.text"
          @click="canviarPagina(index)"
        />
  </template>
  
  <script>
  import OpcionsHabits from './OpcionsHabits.vue';
  import imgSol from '../assets/sunshine.jpg';
  import imgGel from '../assets/icebath.jpg';
  import imgGym from '../assets/training.jpg';
  import imgMeditar from '../assets/meditation.jpg';
  import imgIoga from '../assets/ioga.jpg';
  import imgLlegir from '../assets/read.jpg';

    export default {
        name: 'IniciHabits',
        components: {
            OpcionsHabits,
        },
        data() {
            return {
                habits: [
                    {
                    foto: imgSol,
                    text: 'Exposició al Sol'
                    },
                    {
                    foto: imgGel,
                    text: 'Banys de Gel'
                    },
                    {
                    foto: imgGym,
                    text: 'Entrenament Físic'
                    },
                    {
                    foto: imgMeditar,
                    text: 'Meditar'
                    },
                    {
                    foto: imgIoga,
                    text: 'Ioga'
                    },
                    {
                    foto: imgLlegir,
                    text: 'Llegir'
                    }
                ],
            }
        },
         methods: {
            canviarPagina(index) {
                this.$emit('canviar-pagina', index +1);
                console.log(index +1);
             }
        }
   }
  </script>
  