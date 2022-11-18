<template>
  CONTAINER
  <Create />
</template>


<script>

import { ref } from "vue"
import Create from './Create.vue'
export default {
  components : {
    Create
  },
  setup() {
    let data = ref([
      {name:"Eating"},
      {name:"Drinking"},
      {name:"Sleeping"}
    ])

    function createItem(item) {
      console.log("Container::createItem " + item)
      data.value.push( 
        {name:item}
      )
    }
    function deleteItem(param) {
       console.log("Container::deleteItem " + param)
    }
    return {
      data,
      createItem,
      deleteItem
    }
  }
}

</script>


<style scoped>


</style