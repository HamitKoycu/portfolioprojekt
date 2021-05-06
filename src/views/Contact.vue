<template>
  <v-content>
    <div class="staticHero">
      <v-img src="../assets/images/img58.png">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">Kontakt mig</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Navn"
      required
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>

 <v-textarea
        v-model="message"
      :rules="messageRules"
      label="Besked"
      required
></v-textarea>

    <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Submit
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset
    </v-btn>

  </v-form>
      </v-container>
    </div>
  </v-content>
</template>

<script>
  export default {
    name: 'Contact',
    
  data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Navn er nødvendigt',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail er nødvendigt',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      message: "",
    messageRules: [
      v => !!v || "Besked er nødvendigt",
      v => (v && v.length >= 10) || "Message must be more than 10 characters"
    ],
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
    },
};
</script>
