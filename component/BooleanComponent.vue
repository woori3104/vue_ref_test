<!-- ChildComponent.vue -->
<script>
export default {
  props: {
    isRequire: Boolean
  }
};
</script>

<template>
  <div>{{ isRequire }}</div>
</template>
