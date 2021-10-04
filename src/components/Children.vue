<template>
  <div>Children Component</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Children extends Vue {
  /** ライフサイクルイベント */
  private beforeCreate(): void {
    console.log("Children: beforeCreate");
  }
  private created(): void {
    console.log("Children: created");
  }
  private beforeMount(): void {
    console.log("Children: beforeMount");
  }
  private mounted(): void {
    console.log("Children: mounted");
  }
  private beforeUpdate(): void {
    console.log("Children: beforeUpdate");
  }
  private updated(): void {
    console.log("Children: updated");
  }
  private beforeDestroy(): void {
    console.log("Children: beforeDestroy");
  }
  private destroyed(): void {
    console.log("Children: destroyed");
  }
}
</script>
<style scoped></style>
