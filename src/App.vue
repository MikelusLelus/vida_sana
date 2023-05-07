<template>
  <div>
    <header class="header">
      <h1 class="titol" v-if="paginaActual === 0">Vida Sana</h1>
      <h1 class="titol" v-else-if="paginaActual === 1">Exposició al Sol</h1>
      <h1 class="titol" v-else-if="paginaActual === 2">Banys de Gel</h1>
      <h1 class="titol" v-else-if="paginaActual === 3">Entrenament Físic</h1>
      <h1 class="titol" v-else-if="paginaActual === 4">Meditació</h1>
      <h1 class="titol" v-else-if="paginaActual === 5">Ioga</h1>
      <h1 class="titol" v-else-if="paginaActual === 6">Llegir</h1>

    </header>

    <main class="contingut">
        <IniciHabits 
        v-if="paginaActual === 0"
        @canviar-pagina="canviarPagina"
        />
        <ExpoSol
          v-else-if="paginaActual === 1"
        />
        <BanysGel
          v-else-if="paginaActual === 2"
        />
        <EntrenamentFisic
          v-else-if="paginaActual === 3"
        />
        <Meditar
          v-else-if="paginaActual === 4"
        />
        <Ioga
          v-else-if="paginaActual === 5"
        />
        <Llegir
          v-else-if="paginaActual === 6"
        />
        <BotoHabits 
          v-if="paginaActual !== 0"
          @click="canviarPagina(0)"
        />
    </main>
  </div>
</template>

<script>
import IniciHabits from './components/IniciHabits.vue';
import ExpoSol from './components/ExpoSol.vue';
import BanysGel from './components/BanysGel.vue';
import EntrenamentFisic from './components/EntrenamentFisic.vue';
import Meditar from './components/Meditar.vue';
import Ioga from './components/Ioga.vue';
import Llegir from './components/Llegir.vue';

import BotoHabits from './components/BotoHabits.vue';

export default {
  components: {
    IniciHabits,
    ExpoSol,
    BanysGel,
    EntrenamentFisic,
    Meditar,
    Ioga,
    Llegir,
    BotoHabits,
  },
  emits: ['canviar-pagina'],
  data() {
    return {
      paginaActual: 0,
    }
  },
  methods: {
    canviarPagina(novaPagina) {
      this.paginaActual = novaPagina;
      this.amuntPagina();
    },
    amuntPagina() {
      window.scrollTo(0, 0);
    }   
  }
}
</script>

