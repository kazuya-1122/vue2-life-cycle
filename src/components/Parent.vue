<template>
  <div>
    <button v-if="!hide" @click="toggle">Destroy Children</button>
    <button v-if="hide" @click="toggle">Create Children</button>
    <button @click="onDestroyClick">Destroy</button>
    <Children v-if="!hide"></Children>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Children from "@/components/Children.vue";

@Component({
  components: {
    Children,
  },
})
export default class Parent extends Vue {
  private hide = false;

  private toggle(): void {
    this.hide = !this.hide;
  }
  private onDestroyClick(): void {
    this.$destroy();
  }
  /** ライフサイクルイベント */
  private beforeCreate(): void {
    console.log("Parent: beforeCreate");
  }
  private created(): void {
    console.log("Parent: created");
  }
  private beforeMount(): void {
    console.log("Parent: beforeMount");
  }
  private mounted(): void {
    console.log("Parent: mounted");
  }
  private beforeUpdate(): void {
    console.log("Parent: beforeUpdate");
  }
  private updated(): void {
    console.log("Parent: updated");
  }
  private beforeDestroy(): void {
    console.log("Parent: beforeDestroy");
  }
  private destroyed(): void {
    console.log("Parent: destroyed");
  }
}
</script>
<style scoped></style>
