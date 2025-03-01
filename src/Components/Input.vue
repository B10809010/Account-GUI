<template>
	<input type="text" />
</template>
<script setup>

</script>
<style lang="sass" scoped>
input
  width: 240px;
  height: 40px;
  border-radius: 6px;
  padding: 8px 12px;
  font-size: 1em;
  font-family: inherit;
  color: #000000;
  background: #ffffff;
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.2);
  border: 1px solid #aaaaaa;
  box-sizing: border-box;

input
  cursor: text;

input
  &:focus
    background: #f6f6f6;
    border: 2px solid #000000
</style>