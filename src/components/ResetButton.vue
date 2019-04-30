<template>
  <v-btn @click="onClick">Reset</v-btn>
</template>

<script lang="ts">
    import {
        Component, 
        Emit, 
        Prop, 
        Vue
    } from "vue-property-decorator";

    @Component
    export default class ResetButton extends Vue {
        private initialValue!: string;

        // モデルバインドのために記述必須
        @Prop()
        public value!: string;

        // ライフサイクルフック
        public created() {
            this.initialValue = this.value;
        }

        // モデルバインドのために記述必須
        @Emit()
        public input(value: string) {
        }

        public onClick() {
            this.input(this.initialValue);
        }
    }
</script>