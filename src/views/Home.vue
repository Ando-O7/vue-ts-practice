<template>
  <div class="home">
    <p>{{greetText}}</p>
    <p>
      <MyButton :greet="greetText" @clicked="onMyButtonClicked"></MyButton>
    </p>
    <p>
      <ResetButton v-model="greetText"></ResetButton>
    </p>
  </div>
</template>

<script lang="ts">
  import {
    Component,
    Vue
  } from 'vue-property-decorator';
  import MyButton from '@/components/MyButton.vue';
  import ResetButton from '@/components/ResetButton.vue';

  @Component({
    components: {
      MyButton,
      ResetButton,
    },
  })

  export default class Home extends Vue {
    public greetText: string = 'Hello';

    public onMyButtonClicked() {
      this.greetText = 'こんにちは';
    }
  }
</script>
