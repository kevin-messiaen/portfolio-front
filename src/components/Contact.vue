<template>
	<v-card>
		<v-card-text>
			<div>Contact</div>
			<p class="display-1 text--primary">
				{{ contact.firstname }} {{ contact.lastname }}
			</p>
			<v-btn
				text
				:href="`mailto:${contact.mail}`">
				<v-icon>mdi-mail</v-icon>
				<span class="mr-2">{{ contact.mail }}</span>
			</v-btn>
			<v-btn
				text
				:href="`tel:${contact.phone}`">
				<v-icon>mdi-phone</v-icon>
				<span class="mr-2">{{ contact.phone }}</span>
			</v-btn>
		</v-card-text>
	</v-card>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Contact',
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