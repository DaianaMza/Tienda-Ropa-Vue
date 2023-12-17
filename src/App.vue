<script>
import Navbar from './components/Navbar';

export default {
  name: 'App',

  components: {
    Navbar,
  },

  data: () => ({
    //
  }),
};
</script>

<template>
  <v-app>
    <v-main>
      <Navbar />
      <v-container fluid>
        <v-row>
          <v-col cols="12">
            <v-card>
              <v-img src="./assets/verde.jpg" max-height="10%" max-width="100%" contain>
                <v-card-title class="top ml-10">
                  <div class="one">
                    <h1>Nuevo</h1>
                  </div>

                </v-card-title>
              </v-img>
            </v-card>
          </v-col>
        </v-row>

        <div class="contenedor-tarjetas">
          <article class="tarjetabody">
            <figure><img class="imagencartera" src="https://pngimg.com/uploads/women_bag/women_bag_PNG6428.png" alt="">
            </figure>
          </article>
          <article class="tarjetabody">
            <figure><img class="imagenzapato"
                src="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.pngall.com%2Fwp-content%2Fuploads%2F2016%2F03%2FShoes-PNG-Image.png&f=1&nofb=1&ipt=a6f0856193ff5a54a6756c3e56e480a8a706dc55fefbaf779d9abb5be2f74739&ipo=images"
                alt=""></figure>
          </article>
          <article class="tarjetabody">
            <figure><img class="imagenvestido"
                src="https://static.trendme.net/pictures/items/GUCCI_Haljine-Danijela-full-36272-672395.png" alt="">
            </figure>
          </article>
          <article class="tarjetabody">
            <figure><img class="imagenacc"
                src="http://www.lunettedemarque.fr/wp-content/uploads/2016/01/lunettes-de-soleil-gucci-homme-1.png"
                alt=""></figure>
          </article>
        </div>
      </v-container>

    </v-main>
  </v-app>
</template>

<style>
h1 {
  position: absolute;
  padding-top: 50px;
  margin: 0;
  font-family: "Raleway", sans-serif;
  font-weight: 300;
  font-size: 60px;
  color: #ffffff;
}


.one h1 {
  text-align: center;
  text-transform: uppercase;
  padding-bottom: 5px;
}

.one h1:before {
  width: 28px;
  height: 5px;
  display: block;
  content: "";
  position: absolute;
  bottom: 3px;
  left: 50%;
  margin-left: -14px;
  background-color: #ffffff;
}

.one h1:after {
  width: 100px;
  height: 1px;
  display: block;
  content: "";
  position: relative;
  margin-top: 25px;
  left: 50%;
  margin-left: -50px;
  background-color: #ffffff;
}

.contenedor-tarjetas {
  display: flex;
}

.tarjetabody {
  padding-top: 15px;
  margin-right: 20px;
}

.tarjeta {
  font-weight: 400;
  margin: 2rem 0 0.25rem 0;
}

figure {
  width: 400px;
  aspect-ratio: 8 / 5;
  --bg: hsl(200, 80%, calc(90% - (var(--hover) * 10%)));
  --accent: hsl(129, 80%, 40%);
  transition: background 0.2s;
  background: radial-gradient(circle at top left, var(--accent), transparent 75%),
    var(--bg);
  margin: 0;
  position: relative;
  overflow: hidden;
  border-radius: 1.5rem;
}

figure:after {
  content: "";
  position: absolute;
  width: 20%;
  aspect-ratio: 1;
  border-radius: 50%;
  bottom: 0%;
  left: 10%;
  background: linear-gradient(-65deg, var(--bg) 50%, var(--accent) 50%);
  filter: blur(25px);
  transform:
    translateX(calc(var(--hover) * 15%)) scale(calc(1 + (var(--hover) * 0.2)));
  transition: transform 0.2s, background 0.2s;
}

.imagencartera {
  position: absolute;
  left: 20%;
  top: 10%;
  width: 70%;
  transform:
    translateX(calc(var(--hover) * -15%)) scale(calc(1 + (var(--hover) * 0.2)));
  transition: transform 0.2s;
}

.imagenzapato {
  position: absolute;
  left: 20%;
  top: 35%;
  width: 79%;
  transform:
    translateX(calc(var(--hover) * -15%)) scale(calc(1 + (var(--hover) * 0.2)));
  transition: transform 0.2s;
}

.imagenvestido {
  left: 20%;
  top: 55%;
  width: 79%;
  transform:
    translateX(calc(var(--hover) * -15%)) scale(calc(1 + (var(--hover) * 0.2)));
  transition: transform 0.2s;
}

.imagenacc {
  position: absolute;
  left: 10%;
  top: 25%;
  width: 79%;
  transform:
    translateX(calc(var(--hover) * -15%)) scale(calc(1 + (var(--hover) * 0.2)));
  transition: transform 0.2s;
}

article {
  --hover: 0;
}

article:hover {
  --hover: 1;
}
</style>

