<template>
  <v-row>
    <v-col class="cafe__component">
      <h1 class="py-4">List of cafes</h1>
      <v-row class="cafe__list mx-2">
        <v-col v-for="cafe in cafes" :key="cafe.id" md="4" xl="4">
          <v-card class="cafe__card">
            <v-img height="250" :src="cafe.img"> </v-img>
            <v-card-title>
                <router-link to="/cafe/view">{{ cafe.name }}
                </router-link>
            </v-card-title>
            <v-card-text>
              <p>{{ cafe.description }}</p>
              <b>Rating: {{ cafe.rating }}</b>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  name: "Cafe",
  data: () => ({
    cafes: [
      {
        id: 0,
        name: "K-FOOD",
        description: "Here",
        img: "https://indo-europeanfoods.com/wp-content/uploads/2020/01/indo-chinese-food.jpg",
        tags: ["asian"],
        rating: 5,
      },
      {
        id: 1,
        name: "WOOD",
        description: "woody",
        img: "https://ak.picdn.net/shutterstock/videos/12193973/thumb/1.jpg",
        tags: ["woodian"],
        rating: 1,
      },
      {
        id: 2,
        name: "R-FOOD",
        description: "Russian food",
        img: "https://www.56thparallel.com/wp-content/uploads/2018/11/Russian-food.jpg",
        tags: ["russian"],
        rating: 6,
      },
    ],
  }),
};
</script>
