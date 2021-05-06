<template>
  <v-content>
    <div class="staticHero">
      <v-img src="../assets/images/img10.png">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">Omkring Mig</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container class="text-center">
        <youtube :video-id="videoId" ref="youtube" @playing="playing"></youtube>
<button @click="playVideo"></button>
        <p>Mit navn er Hamit Köycü, hvilket kan være ret svært og udtale. Jeg er den dansk-tyrkiske ambitiøse, kvalitetsbevidste og energiske fyr, som har levet i hele 23 somre. Skal jeg gå mere i dybden med mine personlige kompetencer og hvem jeg i det hele taget egentlig er?  - Så læs med. Jeg er en person som er målrettet når det gælder livet, men også på arbejdspladsen. Personen som er struktureret og hurtigt danner nye vaner samt rutiner når jeg starter et nyt kapitel i livet. Samtidig er jeg meget hjælpsom og åben overfor andre mennesker jeg møder, da det ligger mig meget nært, i forhold til den anden del af kulturen jeg har med i rygsækken. Jeg er glad for, at have fået muligheden for at have to forskellige kulture i mig. Det er lige præcis det, som gør mig speciel og danner hvem jeg er som person. Lyder jeg, som en profil du eller dit team gerne vil høre mere om?  - Så smid mig gerne en mail eller ring mig op! Jeg er kun en SMS væk fra jer.  </p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">That's me</h2>
        <v-row>
          <v-col v-for="item in items" :key="item.id" class="d-flex child-flex">
            <v-card flat tile class="mx-auto deep-orange lighten-1">
              <v-img :src="item.src" aspect-ratio="1" class="grey lighten-2"></v-img>
              <v-card-text class="text--primary text-center">
                <div class="title">{{ item.name }}</div>
                
                <a :href="item.URLlink">
                <p>{{ item.title }}</p></a>
              </v-card-text>

            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-content>
</template>

<script>
  export default {
    name: 'About',
    
  data() {  
     return {
        videoId: '4miJaENj7V4',
       items: [  {
          id: 1,
          src: require("../assets/images/img51.png"),
          name: 'CV',
          title: "Klik her for at downloade mit CV",
          URLlink: "../assets/images/bcard.pdf"
        },
        {
          id: 1,
          src: require("../assets/images/img.11.jpeg"),
          name: 'Hamit Köycü',
          title: "Multimediedesigner / SoMe annoncører"
        },
         {
          id: 1,
          src: require("../assets/images/img55.png"),
          name: 'Business card',
          title: "Klik her for at downloade mit Business card",
          URLlink: "../assets/images/cv.pdf"
        },
      ]
    };
  }
};
</script>
