<template>
  <div id="app">
    <MoviesAPI></MoviesAPI>
    <div id="team" class="container-fluid">
      <div class="row justify-content-center mb-5">
        <div class="col mt-5" v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TeamCard from "./components/TeamCard.vue"
import MoviesAPI from './components/MoviesAPI.vue'

export default {
  name: 'App',
  components:{
    TeamCard,
    MoviesAPI
  },
  data(){
    return {
      team: [
        {
          codigo: 1,
          nombre: "David Ruiz Rubiano",
          descripcion:
            "David es estudiante de ingeniería en Telemática de la Universidad Distrital Francisco José de Caldas de Bogotá. Es un apasionado por la tecnología en general, entre otros, el software Libre, Aplicaciones Móviles, Redes de Datos, Seguridad Informática y el Internet de las cosas. Tiene experiencia trabajando en la administración y configuración de infraestructura de TI, también en el sector de Automatización industrial. Le gusta leer novelas y series de suspenso y acción. Sus pasatiempos son montar bicicleta, ver series y jugar videojuegos. También posee interés por las artes en general, le apasiona el teatro, lo ha practicado por varios años y a nivel musical le ha interesado la percusión. Escucha música alternativa, en especial los géneros: rock, pop y electrónica. También es apasionado por el mundo del café y está en proceso de convertirse en un excelente Barista.",
          rol: "Scrum Master",
          image: require('./assets/img/brayan_r.jpeg'),
        },
        {
          codigo: 2,
          nombre: "Paulo Rivera Gil",
          descripcion:
            "Paulo tiene 21 años, vive en la ciudad de Ibagué (Tolima), es estudiante de Matemáticas con Enfasis en Estadistica en la Universidad del Tolima, además le gustan los cursos de Inglés y se desempeña muy bien en ese campo, desde su corta edad le ha interesado todo lo relacionado con las tecnologías y la computación. Sus intereses están enfocados en jugar videojuegos como Fortnite (un videojuego desarrollado por la empresa Epic Games, su modo más popular es Fortnite Battle Royale, donde hasta cien jugadores luchan en una isla, en espacios cada vez más pequeños debido a la tormenta, para ser la última persona en pie), practicar fútbol, viajar y conocer nuevos lugares. De los lugares que ha conocido, su favorito es Los Pinos, que está ubicado en Gigante (Huila), y algún día sueña con conocer Hawái.",
          rol: "Tester",
          image: require('./assets/img/paulo_r.jpeg'),
        },
        {
          codigo: 3,
          nombre: "David Peralbo Florez",
          descripcion:
            "David tiene 29 años, vive en Barranquilla, a lo largo de su vida ha realizado distintos cursos de programación web y ha dado algunos pasos en lenguajes específicos como Java y SQL, también tiene bastante facilidad para el manejo de los idiomas (como el inglés) y además le gusta dedicar parte de su tiempo para aprender otros, actualmente está interesado en el aprendizaje del alemán. Entre sus pasatiempos está el aprender a realizar animaciones como las existentes en varios videojuegos (especialmente aquellas hechas en 3D), otra de sus actividades predilectas está relacionada con cualquier pasatiempo para aprender acerca de la historia mundial. Su civilización favorita es la Griega (se considera generalmente como la cultura que sirvió de base a la civilización occidental).",
          rol: "Arquitecto de software",
          image: require('./assets/img/david_m.jpeg')
        },
        {
          codigo: 4,
          nombre: "Andrés Díaz Genis",
          descripcion:
            "Andrés actualmente es estudiante de Ingeniería Mecatrónica en la Universidad Tecnológica de Bolívar, tiene 19 años y siempre le han atraído las áreas relacionadas con la computación, aunque estudia en Cartagena, su lugar de residencia es Sabanalarga (Atlántico). Entre sus pasatiempos principales están jugar videojuegos como League of Legends (un juego muy competitivo y rápido con acción y estrategia diseñado para aquellos que ansían una victoria bien merecida) o Age of Empires (una serie de videojuegos de estrategia en tiempo real, donde se pueden ver varios tipos de civilizaciones las cuales dependiendo de su elección le favorecerán ciertas estrategias), ver series o películas (su película favorita es la saga de El Hobbit), escuchar música (aunque no tiene un género favorito) y obviamente estudiar.",
          rol: "Desarrollador frontend",
          image: require('./assets/img/andres_d.jpeg',)
        },
        {
          codigo: 5,
          nombre: "Andrés Cantor Sierra",
          descripcion:
            "Andrés estudió Licenciatura en Matemáticas en la Universidad Pedagógica Nacional y realizó una especialización en Gerencia Educativa en la Universidad de La Sabana. Actualmente tiene 43 años y toda su vida ha vivido en Bogotá. Siempre ha contado como una de sus aficiones todo lo relacionado con la programación y la forma en que lo puede relacionar o no, con su profesión. Disfruta montar en bicicleta, ver series (entre sus favoritas están GOT, Sherlock, Punisher, Sense 8, Dragon Ball, Naruto y Bleach), leer un buen libro (especialmente sagas como El señor de los anillos, Harry Potter, GOT o cualquier otro buen libro que pueda encontrar), además de escuchar música para acompañar las actividades diarias (Música Electrónica, Rock, Pop o una buena Salsa que por supuesto le encanta bailar).",
          rol: "Desarrollador backend",
          image: require('./assets/img/andres_c.png',)
        },
      ],
    };
  }
}
</script>

