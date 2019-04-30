<template>
  <v-btn @click="onClick">MyButton</v-btn>
</template>

<script lang="ts">
  import {
    Component,
    Emit,
    Prop,
    Vue,
  } from 'vue-property-decorator';

  @Component
  export default class MyButton extends Vue {
    private count: number = 0;

    @Prop()
    public greet ? : string;

    @Emit()
    public click(count: number) {}

    public onClick() {
        this.count++;
        this.click(this.count);
    }
  }

</script>
