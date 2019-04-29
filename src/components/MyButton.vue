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
    @Prop()
    public greet ? : string;

    @Emit()
    public clicked() {}

    public onClick() {
      alert(this.greet);
      this.clicked();
    }
  }

</script>
