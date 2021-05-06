<template>
  
   <div class="block latestPostBlock">
       <v-container>
     <h2 class="text-center">Mine sidste cases</h2>
     <v-row>
       <v-col v-for="item in items" :key="item.id" cols="12" md="4">
                        <v-card
                    class="mx-auto"
                    max-width="400"
                  >
                    <v-img
                      class="white--text align-end"
                      height="200px"
               :src="item.src"
                    >
                      <v-card-title>{{ item.title }}</v-card-title>
                    </v-img>

                    <v-card-subtitle class="pb-0">{{ item.title }}</v-card-subtitle>

                    <v-card-text class="text--primary">
                      <div>{{ item.description }}</div>
                    </v-card-text>

                    <v-card-actions>
                      <v-btn
                        color="primary"
                        text
                      >
                        Læs mere
                      </v-btn>
                    </v-card-actions>
                  </v-card>
        </v-col>
      </v-row>
      </v-container>
     </div>
 
</template>

<script>
  export default {
    name: 'LatestPost',

     data() {
    return {
      items: [
              {
        id: 1,
        title: "Padelsol",
        subtitle: "Logo design og Brochure",
        description: "Padelsol er en dansk virksomhed, som befinder sig i Spanien. Casen lød på et logo design til virksomheden, samt en brochure...",
        src: require("../assets/images/img21.png")
      },
      {
        id: 2,
        title: "Nordicpixel",
        subtitle: "Nordicpixel",
        description: "Nordicpixel er et marketing bureau, som rådgiver andre virksomheder med markedsføring via de sociale medier. Casen lød på et nyt logo og rebranding...",
        src: require("../assets/images/img1.png")
      },
      {
        id: 3,
        title: "Easyscoop",
        subtitle: "Easyscoop",
        description: "Easyscoop er en dansk web-shop, som sælger scoops til hundeejere. Casen lød på at virksomheden havde brug for hjælp til...",
        src: require("../assets/images/img2.jpg")
      }
      ,{
        id: 4,
        title: "Oceaneye",
        subtitle: "Oceaneye",
        description: "Denne opgave er blevet udarbejdet i forbindelse med Multimediedesignernes 1. semester projekt 2020, hvor emnet var ‘Havet’...",
        src: require("../assets/images/img13.png")
      }
      ,{
        id: 5,
        title: "Kortfilm",
        subtitle: "Kortfilm",
        description: "Denne opgave er blevet udarbejdet af min gruppe og jeg. Vi filmede en kortfilm med fokus på genreren horror...",
        src: require("../assets/images/img19.png")
      }
      ,{
        id: 6,
        title: "7-kanten SoMe",
        subtitle: "7-kanten SoME",
        description: "Denne opgave for 7-kanten omhandlede deres SoMe kanneler. Hvordan de kunne rebrande sig selv, og være med på moden...",
        src: require("../assets/images/img20.png")
      }
      ]
    };
  }
};
</script>
