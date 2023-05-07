<template>
    <div class="opcions-habits">
      <img :src="foto" alt="Imatge de l'opció de hàbits">
      <p>{{ text }}</p>
    </div>
  </template>
  
  <script>
    export default {
        name: 'OpcionsHabits',
        props: {
        foto: {
            type: String,
            required: true
        },
        text: {
            type: String,
            required: true
        }
        }
    }
  </script>
  
<style scoped>
.opcions-habits {
    position: relative;
    display: inline-block;
    width: calc((100vw / 4));
    margin: 5px;
    text-align: center;
}

.opcions-habits img {
    display: block;
    height: calc((100vw / 3));
    width: 100%;
    object-fit: cover;
    object-position: center;
    margin-bottom: 10px;
}

.opcions-habits p {
  font-family: 'Roboto', sans-serif;
  font-weight: bold;
  position: absolute;
  bottom: 6%;
  right: 0;
  width: 100%;
  color: white;
  margin: 0;
  font-weight: bold;
  font-size: 18px;
}

.opcions-habits:hover img {
  opacity: 0.3;
  cursor: pointer;
}

.opcions-habits:hover p{
  color: black;
}


</style>

  