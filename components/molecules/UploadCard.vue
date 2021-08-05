<template>
  <form
    action="https://formsubmit.co/zop.assets@gmail.com"
    method="POST"
    class="upload-card"
    name="_autoresponse"
  >
    <input type="hidden" name="_captcha" value="false" />
    <input type="hidden" name="_next" value="http://localhost:3000/z/profile" />
    <input
      id="file-button"
      type="file"
      hidden
      required
      @change="onFileChange"
    />
    <div class="file-content">
      <label for="file-button" class="file-button">Procurar arquivo</label>
      <!-- eslint-disable-next-line vue/no-v-html --><!-- eslint-disable-next-line prettier/prettier -->
      <div v-show="upload === true" v-html="$feathericons['check'].toSvg()"></div>
    </div>
    <input type="submit" class="send-button" value="Enviar" />
  </form>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      upload: false
    }
  },
  methods: {
    onFileChange() {
      this.upload = true
    }
  }
})
</script>

<style lang="scss" scoped>
.upload-card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 40px;

  background: color(black, 'dark');
  border-radius: 8px;

  flex: none;
  order: 1;
  flex-grow: 0;
  gap: 32px;
  margin: 64px 0px;
  max-width: 440px;
  .file-content {
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
    align-items: center;
    gap: 4px;
    color: color(zop);
  }
  .send-button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 20px 44px;

    /* zop/base */
    background: color(zop);
    color: color(black, 'darkest');
    font-weight: 600;
    font-size: 16px;
    gap: 12px;
    cursor: pointer;

    border-radius: 16px;

    /* Inside Auto Layout */
    flex: none;
    order: 1;
    flex-grow: 0;
    margin: 0px 32px;
    p {
      font-weight: 600;
    }
    &:hover {
      background: rgba(83, 112, 254, 0.8);
    }
  }
  .file-button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 20px 44px;

    /* zop/base */
    background: color(black, 'light');
    color: color(white, 'light');
    font-weight: 600;

    gap: 12px;
    cursor: pointer;

    border-radius: 16px;

    /* Inside Auto Layout */
    flex: none;
    order: 1;
    flex-grow: 0;
    p {
      font-weight: 600;
    }
    &:hover {
      background: #303030;
    }
  }
}
</style>
