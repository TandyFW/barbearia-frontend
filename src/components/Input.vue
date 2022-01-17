<template>
  <div class="input-container">
    <label>{{ backLabel }}</label>
    <input :type="type" :placeholder="placeholder" />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    placeholder: String,
    backLabel: String,
    type: String,
  },
  type: {
    default: "text",
  },
})
export default class Input extends Vue {
  placeholder!: string;
  backLabel!: string;
  type!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.input-container {
  // border: 1px solid blue;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 2px;
  label {
    // border: 1px solid green;
    text-align: left;
    color: black;
    font-size: 24px;
    width: 50%;
  }
  input {
    width: 100%;
    box-sizing: border-box;
    height: 32px;
    font-size: 18px;
  }
}
</style>
