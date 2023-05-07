<template>
  <div>
    <div class="aplicacio">
    <Temporitzador 
    :minuts="3"
    :audio-src="musica" />
    </div>
    <div class="text_explicatiu">
    <p>
    Els banys de gel són una pràctica en la qual s'exposa el cos a temperatures fredes, ja sigui a través d'una dutxa o d'un bany de gel. Aquesta pràctica té diversos beneficis, com ara augmentar l'energia i la concentració, construir resiliència i determinació, millorar l'estat d'ànim i augmentar el metabolisme.
    </p>
    <p>
    Exposar-se al fred pot provocar la alliberació d'adrenalina i noradrenalina, el que pot fer que una persona es senti alerta i incrementi l'energia i la concentració. A més, també pot ajudar a controlar el cervell de manera més conscient, el que pot millorar la capacitat de superar els reptes i d'actuar de manera decidida. Els banys de gel també provoquen la alliberació de dopamina, que fa millorar l'estat d'ànim i la concentració. 
    </p>
    <p>
    Un altre efecte positiu dels banys de gel és que poden millorar el sistema immune, el que ajuda a prevenir malalties i infeccions. Això es deu a que l'exposició al fred pot estimular la producció de glòbuls blancs, que són les cèl·lules de defensa del nostre cos. Això significa que si ens acostumem als banys de gel, el nostre cos pot ser més fort per combatre virus i altres agents patògens.
    </p>
    <p>
    Pel que fa el temps, es recomana prendre un bany de gel una vegada per setmana durant 1-3 minuts per a millorar la resiliència, 2 vegades per setmana durant 11 minuts en total per augmentar el metabolisme i durant 3-6 minuts després de fer exercici per a una millor recuperació.
    </p>
    <p>
    La temperatura recomanada per a un bany de gel és molt personal. La llei bàsica es una temperatura que et vulgui sortir d’allà però que sàpigues que pots estar-hi de forma segura.
    </p>
    </div>
  </div>
</template>

<script>
import Temporitzador from './Temporitzador.vue'; 
import musicaIce from '../assets/icebath.mp3';

  export default {
    name: 'BanysGel',
    components: {
        Temporitzador,
     },
     data () {
      return {
        musica: musicaIce,
      }
     }
  }
</script>
