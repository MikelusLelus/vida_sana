<template>
    <div class="marge_llibres">
      <div class="imgMida">
        <a :href="link" target="_blank">
        <img :src="imageSrc">
        </a>
      </div>  
      <div class="titol-boto">
        <span class="estil_titol">{{ imageTitle }} </span> 
      </div>
    </div>
  </template>
  
  <script>
    export default {
      name: 'ImageTitol',
      props: {
        imageTitle: {
          type: String,
          required: true,
        },
        imageSrc: {
          type: String,
          required: true,
        },
        link: {
          type: String,
          required: true,
        }
      },
    };
  </script>
  
  <style>

    .imgMida {
        padding: 20px ;
    }

    .imgMida:hover {
        opacity: 0.4;
    }
    .imgMida img {
        width: 13vw;
        height: 20vw;
    }
    .marge_llibres {
         margin: 10px 40px;
    }
  
  </style>
  