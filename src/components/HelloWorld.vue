<template>
  <h1>Zainan Victor Zhou</h1>

  <div class="zzn-main">
    <p>
      Hey friend, thank you for visiting my personal site.
      Here is a stream of my thoughts and ideas.
    </p>

  </div>
  <div class="flex justify-center space-x-4 w-full">
    <button class="bg-green-500 hover:bg-green-700 py-2 px-4 rounded-full"
            @click="contactBtn">
      Email
    </button>
    <button class="bg-green-500 hover:bg-green-700 py-2 px-4 rounded-full"
            @click="bookTimeBtn">
      Book time
    </button>
  </div>

</template>
<script setup lang="ts">
import { event, pageview } from 'vue-gtag';
pageview({ page_path: '/' });

function contactBtn() {
  console.log(`Clicked contact button.`);
  event('contact_btn_clicked');
  window.open("mailto://contact@zzn.im", '_blank');
};

function bookTimeBtn() {
  console.log(`Clicked bookTimeBtn button.`);
  event('book_time_btn');
  window.open("https://calendly.com/zainan/15min", '_blank');
};

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
</style>
