<!-- src/components/List.vue -->
<template>
  <v-container>
    <!-- Создаем контейнер внутри которого и будут элементы компонента -->

    <v-row class="list__cafes-title">
      <!-- В это row выводим заголовок компонента -->
      <v-col>
        <h2 class="text-center text-h3 py-3">List of cafes</h2>
      </v-col>
    </v-row>

    <v-row class="list__cafes-content">
      <v-col md="4" v-for="item in items_list" :key="item.id">
        <v-card>
          <v-img height="250" :src="item.img"></v-img>
          <!-- С помощью v-img добавляем изображение карточки -->

          <v-card-title>
            <!-- Заголовок заведения -->
            <h3 class="text-h4">{{ item.title }}</h3>
          </v-card-title>

          <v-card-text>
            <!-- Описание заведения -->
            <p class="text-body-1">{{ item.description }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  name: "List",
  data: () => ({
    items_list: [
      {
        id: 0,
        title: "Заведение 1",
        description:
          "Это наверное самое крутое заведение которое вы можете знать",
        img: "", // Здесь добавляем любое изображение
      },
      {
        id: 1,
        title: "Заведение 2",
        description: "Lorem ipsum",
        img: "", // Здесь добавляем любое изображение
      },
      // Дальше можете добавить другие заведения в список
    ],
  }),
};
</script>