<template>
  <div class="hello">
    <slot-test></slot-test>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import SlotTest from '../views/slot/SlotTest.vue';

@Component({
  components: {
    SlotTest,
  }
})
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
