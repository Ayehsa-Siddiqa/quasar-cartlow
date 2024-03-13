<template>
       <div class="col-xs-12 col-sm-6 col-md-3" v-for="item in productsArr" :key="item">
           <q-img :src="item.pic" width="100%"   class="rounded-borders" /> 
       </div>
</template>

<script>
import { useLink } from 'vue-router';

export default {
  // name: 'ComponentName',
  data () {
    return {}
  },
  props:{
     productsArr:Array
  }
}
</script>
