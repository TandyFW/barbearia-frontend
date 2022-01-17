<template>
  <button :id="id" class="btn" :type="type" @click="this.onClick()">
    {{ text }}
  </button>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import { Prop } from "vue-property-decorator";

@Options({
  props: {
    text: String,
    type: String,
    id: String,
  },
})
export default class Button extends Vue {
  // eslint-disable-next-line @typescript-eslint/no-empty-function
  @Prop({ type: Function, default: () => {} })
  // eslint-disable-next-line @typescript-eslint/ban-types
  private onClick!: () => {};
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.btn {
  background-color: whitesmoke;
  width: 20%;
  align-self: flex-end;
}
</style>
