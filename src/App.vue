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
                  <h2 class="title1">NUEVA TEMPORADA</h2>
                </v-card-title>
              </v-img>
            </v-card>
          </v-col>
        </v-row>

        <article class="tarjetabody">
          <figure><img src="https://pngimg.com/uploads/women_bag/women_bag_PNG6428.png" alt=""></figure>
        </article>
      </v-container>



    </v-main>
  </v-app>
</template>

<style>
.tarjetabody {
  padding-top: 15px;
}

.tarjeta {
  font-weight: 400;
  margin: 2rem 0 0.25rem 0;
}

figure {
  width: 400px;
  aspect-ratio: 8 / 5;
  --bg: hsl(330 80% calc(90% - (var(--hover) * 10%)));
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

img {
  position: absolute;
  left: 20%;
  top: 15%;
  width: 40%;
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

