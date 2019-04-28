<template>
  <div class="home">
    <MyButton></MyButton>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MyButton from '@/components/MyButton.vue';

@Component({
  components: {
    MyButton,
  },
})
export default class Home extends Vue {}
</script>
