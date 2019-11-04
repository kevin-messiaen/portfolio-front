<template>
  <div id="contact" class="container pt-8">
    <v-row justify="center">
      <v-col cols="12" md="6">
        <v-form ref="form" v-model="valid">
          <p class="display-1">Me contacter:</p>
          <v-text-field v-model="name" :rules="nameRules" label="Nom" required></v-text-field>
          <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
          <v-textarea v-model="message" :counter="500" :rules="messageRules" label="Message" required></v-textarea>
          <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">Envoyer</v-btn>
        </v-form>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    name: "",
    nameRules: [v => !!v || "Le prénom est requis"],
    email: "",
    emailRules: [
      v => !!v || "L'adresse e-mail est requise",
      v => /^.+@.+\..+$/.test(v) || "L'adresse e-mail doit être valide"
    ],
    message: "",
    messageRules: [
      v => !!v || "Le contenue du message est requis",
      v => v.length < 500 || "Le message ne doit pas dépasser 500 charactères"
    ]
  }),

  methods: {
    validate() {
      if (this.$refs.form.validate()) {
        this.snackbar = true;
      }
    }
  }
};
</script>

<style>
</style>