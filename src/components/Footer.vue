<template>
  
       <v-container>
                      <v-footer
                      padless
                    >
                      <v-card
                        flat
                        tile
                        class=" text-center"
                      >
                        <v-card-text>
                          <v-btn
                            v-for="icon in icons"
                            :key="icon"
                            class="mx-4 "
                            icon
                          >
                            <v-icon size="24px">
                              {{ icon }}
                            </v-icon>
                          </v-btn>
                        </v-card-text>

                        <v-card-text class=" pt-0">
                          Alle rettigheder forbeholdes. Kopiering fra elementer og opgaver må kun finde sted på institutioner eller virksomheder, der har indgået aftale med Hamit Köycü, og kun inden for de rammer, der er nævnt i aftalen. Undtaget herfra er korte uddrag til anmeldelse.
                        </v-card-text>

                        <v-divider></v-divider>

                        <v-card-text>
                          {{ new Date().getFullYear() }} — <strong>HAMIT KÖYCÜ PORTFOLIO PROJEKT</strong>
                        </v-card-text>
                      </v-card>
                    </v-footer>
      </v-container>
</template>

<script>
  export default {
    name: 'Footer',

 data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
};
</script>
