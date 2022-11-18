<template>
  <form>
    <input type="text" v-model="item" />
    <button>Create</button>
  </form>
</template>

<script>
import { ref} from 'vue'
export default {
  let item = ref('')
  setup() {
    return {
      item
    };
  },
};
</script>
