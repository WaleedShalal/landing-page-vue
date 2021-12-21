<template>
  <button class="chat__button d-flex justify-content-center align-items-center">
    <fa :icon="['fas', 'comment-alt']" />
  </button>
</template>

<script>
export default {
  name: "ChatButton",
};
</script>

<style scoped>
.chat__button {
  position: fixed;
  right: 5px;
  bottom: 5px;
  width: 55px;
  height: 55px;
  border-radius: 50%;
  background-color: #ffd04c;
  border: none;
  font-size: 25px;
  color: #33475b;
  z-index: 100;
}
</style>
