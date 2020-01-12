<template>
  <div>
      <slot name="header" :val="msg"></slot>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';

@Component
export default class SlotChild extends Vue {
  @Prop() private msg: string = '자식에서 넘겨준 text!';
}
</script>
