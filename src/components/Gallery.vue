<template>
   <div class="block galleryBlock">
      <v-container>
     <h2 class="text-center">Portfolio</h2>
          <v-row>
        <v-col
          v-for="items in items"
          :key="items.id"
          class="d-flex child-flex"
          cols="6" md="4"
        >
          <v-img
            :src="items.src"
            aspect-ratio="1"
            class="grey lighten-2"
          >
            <template v-slot:placeholder>
              <v-row
                class="fill-height ma-0"
                align="center"
                justify="center"
              >
                <v-progress-circular
                  indeterminate
                  color="grey lighten-5"
                ></v-progress-circular>
              </v-row>
            </template>
          </v-img>
        </v-col>
      </v-row>
      </v-container>
     </div>
     
</template>

<script>
  export default {
    name: 'Gallery',

     data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/img1.png")
        },
        {
          id: 2,
          src: require("../assets/images/img2.jpg")
        },
        {
          id: 3,
          src: require("../assets/images/img3.jpg")
        },
        {
          id: 4,
          src: require("../assets/images/img4.jpg")
        },
        {
          id: 7,
          src: require("../assets/images/img7.png")
        },
        {
          id: 8,
          src: require("../assets/images/img14.png")
        },
        {
          id: 9,
          src: require("../assets/images/img15.png")
        },
        {
          id: 10,
          src: require("../assets/images/img16.png")
        },
        {
          id: 11,
          src: require("../assets/images/img17.png")
        },
        {
          id: 12,
          src: require("../assets/images/img18.png")
        },
         {
          id: 13,
          src: require("../assets/images/img22.jpg")
        },
        {
          id: 14,
          src: require("../assets/images/img56.png")
        },
      ]
    };
  }
};
</script>
