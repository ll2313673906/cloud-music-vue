<template>
  <div>
    <v-row>
      <v-col
        v-for="(item, i) in items"
        :key="i"
        cols="6"
      >
        <v-card
          :color="item.color"
          dark
        >
          <div class="d-flex flex-no-wrap justify-space-between">
            <div>
              <v-card-title
                class="headline"
                v-text="item.title"
              ></v-card-title>

              <v-card-subtitle v-text="item.artist"></v-card-subtitle>
            </div>

            <v-avatar
              class="ma-3"
              size="125"
              tile
            >
              <v-img :src="item.src"></v-img>
            </v-avatar>
          </div>
        </v-card>
      </v-col>
    </v-row>
    <div class="main">
      <v-row class="row-r">
        <v-col
          cols="12"
          class="col-12"
        >
          <v-card
            class="card-right"
            color="#385F73"
            dark
          >
            <v-card-title class="headline">Unlimited music now</v-card-title>

            <v-card-subtitle>Listen to your favorite artists and albums whenever and wherever, online and offline.</v-card-subtitle>
            <img
              src="../assets/images/d.jpg"
              alt="img"
              class="right-img"
            >
          </v-card>

        </v-col>
      </v-row>
      <v-row class="row-r">
        <v-col cols="12">
          <v-card
            class="card-right"
            color="#385F73"
            dark
          >
            <v-card-title class="headline">Unlimited music now</v-card-title>

            <v-card-subtitle>Listen to your favorite artists and albums whenever and wherever, online and offline.</v-card-subtitle>
            <img
              src="../assets/images/c.jpg"
              alt="img"
              class="right-img"
            >
          </v-card>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  data: () => ({
    show: false,
    items: [
      {
        color: '#1F7087',
        src: '../assets/images/c.jpg',
        title: 'Supermodel',
        artist: 'Foster the People'
      },
      {
        color: 'rgb(31,112,135)',
        src: '../assets/images/d.jpg',
        title: 'Halcyon Days',
        artist: 'Ellie Goulding'
      }
    ]
  })
}
</script>

<style scoped lang="scss">
.card-right {
  width: 400px;
  float: left;
}
.col-12 {
  flex-wrap: wrap;
  width: 1900px;
}
.col-12 img {
  width: 100%;
  height: 100%;
}
.row-r {
  width: 300px;
  margin: 20px;
}
.main {
  display: flex;
}
</style>
