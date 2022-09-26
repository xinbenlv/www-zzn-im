<template>
  <h1>Zainan Victor Zhou</h1>

  <div class="zzn-main">
    <p>
      Hey friend, thank you for visiting my personal site.
      Here is a stream of my thoughts and ideas.
    </p>

  </div>
  <div class="flex justify-center space-x-4 w-full">
    <button class="bg-sky-500 hover:bg-sky-700"
            @click="contactBtn">
      Email
    </button>
    <button class="bg-sky-500 hover:bg-sky-700"
            @click="bookTimeBtn">
      Book time
    </button>
  </div>

</template>
<script lang="ts">
import { defineComponent } from 'vue'
import {event} from 'vue-gtag';

export default defineComponent({
  // type inference enabled
  props: {
  },
  mounted() {
  },
  methods: {
    contactBtn(event: Event) {
      console.log(`Clicked contact button.`);
      event('contact_btn_clicked');
      window.open("mailto://contact@zzn.im", '_blank');
    },
    bookTimeBtn(event: Event) {
      console.log(`Clicked bookTimeBtn button.`);
      event('book_time_btn');
      window.open("https://calendly.com/zainan/30min", '_blank');
    }
  },


});
</script>
<style scoped>
.zzn-main {
  max-width: 600px;
  margin: 0 auto;
  text-align: justify;
}
.btn-sm {
  padding: 2px 4px;
}
.bg-sky-500 {
  background-color: #0ea5e9;
}
.hover\:bg-sky-700:hover {
  background-color: #0369a1;
}
</style>
