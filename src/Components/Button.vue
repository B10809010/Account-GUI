<template>
    <button>
        <slot></slot>
    </button>
</template>
<script setup>

</script>
<style lang="sass" scoped>
button
  border-radius: 6px;
  padding: 8px 12px;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  color: #ffffff;
  background: #14591D;
  transition: background 0.25s;
  box-shadow: 0 2px 2px rgba(0, 0, 0, 0.2);
  border: 0px

button
  cursor: pointer;

button
  &:hover
    background: #0A210F;

</style>