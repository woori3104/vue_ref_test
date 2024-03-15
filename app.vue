<!-- ParentComponent.vue -->
<template>
  <ChildComponent :message="parentMessage" />
  <button @click="toggle">Toggle Require</button>
  <BooleanComponent :isRequire="isRequire"/>
</template>

<script setup>
import { ref } from 'vue';
import ChildComponent from './component/ChildComponent.vue';
import BooleanComponent from './component/BooleanComponent.vue';

const isRequire = ref(true);
const parentMessage = ref('Hello from Parent');

function toggle() {
  console.log(`Feature is now ${isRequire.value ? 'disabled' : 'enabled'}`);
  parentMessage.value = isRequire.value + 'Hello from parent"'
  isRequire.value = !isRequire.value;
}
</script>
