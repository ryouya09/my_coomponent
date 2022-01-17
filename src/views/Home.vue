<template>
  <div class="home">
    <BaseTextbox placeName="名前" />
    <BaseCard
      imgPath="/holomythmini.jpg"
      cardDiscription="ホロMyth壁紙"
      urlPath="https://hololive.hololivepro.com/"
      cardWidth="300px"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BaseTextbox from '@/components/baseComponents/BaseTextbox.vue';
import BaseCard from '@/components/baseComponents/BaseCard.vue';

export default defineComponent({
  name: 'Home',
  components: {
    BaseTextbox,
    BaseCard
  },
});
</script>
