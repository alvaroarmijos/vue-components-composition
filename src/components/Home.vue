<template>
  <div>FullName: {{ fullName }}</div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  setup() {
    const firstName = ref("Alvaro");
    const lastName = ref("Armijos");

    const fullName = computed(()=>{
      return `${firstName.value} ${lastName.value}`;
    });
    
    return {
      fullName,
    };
  },
};
</script>