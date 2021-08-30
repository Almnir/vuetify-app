<template>
  <div>
      <v-row>
          <v-col>
              <v-breadcrumbs :items="breadcrumbs_items">

              </v-breadcrumbs>
          </v-col>
      </v-row>
    <v-row>
      <v-col md="5">
        <v-card>
          <v-img
            height="350"
            src="https://russianlife.com/sites/default/cache/file/832A794C-96DC-E22E-1C829B13964DBD3C_fullpage.jpg"
            class="d-flex align-end"
          >
            <v-card-title>
              <h2 class="text-h2 white--text">K-FOOD</h2>
            </v-card-title>
          </v-img>
        </v-card>
      </v-col>
      <v-col md="7">
        <v-card class="h-100">
          <v-card-text>
            <h4 class="text-h5 mb-4">Come here</h4>
            <v-divider></v-divider>
            <p class="mt-4 text-body-1 mr-5">Lorem imsum</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row class="cafe__menu">
      <v-col md="6">
        <v-card> 
            <v-img height="450" src="https://image.shutterstock.com/image-photo/blank-white-dish-on-wood-260nw-428131927.jpg" 
            class="flex align-end">
                <v-card-title>
                    <h2 class="text-h2 white--text">MENU</h2>
                </v-card-title>
            </v-img>
        </v-card>
      </v-col>
      <v-col md="6">
        <v-card> 
           <v-card-text>
               <v-list-item-group>
                   <v-list-item v-for="item in menu_items" :key="item.id">
                       <v-list-item-avatar>
                           <v-img :src="item.img">
                           </v-img>
                       </v-list-item-avatar>
                       <v-list-item-content>
                           <v-list-item-title class="text-subtitle-1">
                               {{item.title}}
                           </v-list-item-title>
                           <v-list-item-title class="text-body-1">
                               {{item.price}}
                           </v-list-item-title>
                       </v-list-item-content>
                       <v-list-item-action>
                           <v-btn icon>
                               <v-icon color="grey lighten-1">
                                   mdi-plus
                               </v-icon>
                           </v-btn>
                       </v-list-item-action>
                   </v-list-item>
               </v-list-item-group>
            </v-card-text> 
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
export default {
  name: "CafeView",
  data: () => ({
      breadcrumbs_items: [
          {
              text: 'Home',
              disabled: false,
              href: '/'
          },
          {
              text: 'K-FOOD',
              disabled: true,
              href: '/cafe/view'
          }
      ],
      menu_items: [
          {
              id: 0,
              title: 'sapporo Miso ramen',
              img: 'https://m.media-amazon.com/images/I/51Wc7cRn-9L.jpg',
              price: 35.99
          },
          {
              id: 1,
              title: 'hueso',
              img: 'https://korshop.ru/upload/iblock/171/17184f1b795821874a6a6978baf61fa9.jpg',
              price: 5.99
          },
          {
              id: 2,
              title: 'possoro huiso',
              img: 'https://m.media-amazon.com/images/I/816ItA4yvpL._SL1500_.jpg',
              price: 3.99
          },
      ]
  })
};
</script>
<style type="text/css">
.h-100 {
  height: 100%;
}
</style>