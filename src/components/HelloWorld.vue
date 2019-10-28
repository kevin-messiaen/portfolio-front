<template>
  <div>
    <h1>Contact</h1>
    <h2>{{ contact.firstname }} {{ contact.lastname }}</h2>
    <p>Mail: {{ contact.mail }}</p>
    <p>Tel.: {{ contact.phone }}</p>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      contact: null
    }
  },
  mounted() {
    axios
      .get('/contact/')
      .then(response => (this.contact = response.data));
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
