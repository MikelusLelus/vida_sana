<template>
    <div>
      <div class="aplicació">
        <div class="columnes-4">
        <ImageTitol 
          v-for="(llibre, index) in llibres"
          :key="index"
          :imageTitle="llibre.titol"
          :imageSrc="llibre.src"
          :link="llibre.url"
        />
        </div>
      </div>
      <div class="text_explicatiu">
      <p>
    La lectura és una activitat que aporta nombrosos beneficis per a la ment i el cos. A través de la lectura, es pot millorar el coneixement, la comprensió i la capacitat d'anàlisi. A més, la lectura pot ajudar a reduir l'estrès i l'ansietat, ja que pot ser una forma de distracció i relaxació. També pot ajudar a millorar la capacitat cognitiva i a ajudar evitar la pèrdua de memòria en la vellesa. La lectura és una activitat flexible que es pot adaptar a les preferències individuals i es pot practicar en qualsevol lloc i moment, amb només un llibre o un dispositiu electrònic.      </p>
      </div>
    </div>
  </template>
  
  <script>
  import ImageTitol from './ImageTitol.vue';
  
  import arteGuerra from '../assets/arte_de_la_guerra.jpg';
  import reglasVivir from '../assets/12_reglas_vivir.jpg';
  import arteMirar from '../assets/arte_de_mirar.jpg';
  import dune from '../assets/dune.jpg';
  import wallStreet from '../assets/wallstreet.jpg';
  import magiaSilencio from '../assets/magia_silencio.jpg';
  import gomorra from '../assets/gomorra.jpg';
  import hombreTiza from '../assets/hombre_tiza.jpg';
  


    export default {
      name: 'Llegir',
      components: {
        ImageTitol,
      },
      data () {
        return {
          llibres: [
            {
              titol: 'Filosofia',
              src: arteGuerra,
              url: 'https://www.casadellibro.com/libro-el-arte-de-la-guerra/9788494709203/7925837?campaignid=15902440796&adgroupid&feeditemid&targetid&matchtype&network=x&device=c&devicemodel&ifmobile%3A%5Bmobile%5D&ifnotmobile%3A%5Bnotmobile%5D=%5Bnotmobile%5D&ifsearch%3A%5Bsearch%5D&ifcontent%3A%5Bdisplay%5D&creative&keyword&placement&target&adposition&gclid=CjwKCAjwitShBhA6EiwAq3RqA6RzC8QiS7j1Ctwy7WIZeVwzG6yxEH3_8hrbv-O00ykNvhMLRg2lvRoCdrMQAvD_BwE',
            },
            {
              titol: 'Autoajuda',
              src: reglasVivir,
              url: 'https://www.casadellibro.com/libro-12-reglas-para-vivir/9788408233114/11652882'
            },
            {
              titol: 'Art',
              src: arteMirar,
              url: 'https://www.casadellibro.com/libro-el-arte-de-mirar/9788417254353/6408240'
            },
            {
              titol: 'Literatura',
              src: dune,
              url: 'https://www.casadellibro.com/libro-dune-nueva-edicion-las-cronicas-de-dune-1/9788466353779/11543708'
            },
            {
              titol: 'Economia',
              src: wallStreet,
              url: 'https://www.casadellibro.com/libro-un-paso-por-delante-de-wall-street-como-utilizar-lo-que-ya-sabes-para-ganar-dinero-en-bolsa/9788423417131/2422908'
            },
            {
              titol: 'Espiritualitat',
              src: magiaSilencio,
              url: 'https://www.casadellibro.com/libro-la-magia-del-silencio/9788408177319/5808338'
            },
            {
              titol: 'Politica',
              src: gomorra,
              url: 'https://www.casadellibro.com/libro-gomorra-un-viaje-al-imperio-economico-y-al-sueno-de-poder-de-la-camorra/9788483468463/1219324'
            },
            {
              titol: 'Novela Negra',
              src: hombreTiza,
              url: 'https://www.casadellibro.com/libro-el-hombre-de-tiza/9788401019814/6409551'
            }
          ]
        }
      }
    }
  </script>

  <style>

  .columnes-4 {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;

  }

  </style>