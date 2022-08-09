<template>
  <span className="user">
    <span className="name">{{ name }}</span>
    <span className="handle">{{ handle }}</span>
  </span>
</template>

<script>
export default {
  props: ["name", "handle"],
};
</script>

<style></style>
