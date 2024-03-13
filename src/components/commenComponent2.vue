<template>
      <div :class="$q-screen-gt-lg ? 'container':'q-px-lg q-pt-xl' ">
          <div class="row" :class="$q.screen.gt.xs? 'q-col-gutter-lg':'q-col-gutter-sm'">
              <div class="col-12">
                <div class="text-h5">{{dataObj.title}}</div>
              </div>
              <div class="col-xs-12 col-sm-8">
                 <q-img :src="dataObj.img1" class="rounded-borders" fit="fill" width="100%" height="100%"/> 
              </div>
              <div class="col-xs-12 col-sm-4">
                <q-img :src="dataObj.img2" class="rounded-borders" fit="fill" width="100%" height="100%"/>
              </div> 
              <div class="col-xs-12 col-sm-4">
                <q-img :src="dataObj.img3"  class="rounded-borders"  fit="fill" width="100%" height="100%"/>
              </div>
              <div class="col-xs-12 col-sm-8">
                <q-img :src="dataObj.img4"  width="100%" class="rounded-borders" fit="fill" wi height="100%"/>
               </div>
          </div>
        
      </div>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup () {
    return {}
  },
  props:{
   dataObj:Object,
  },
  data(){
    return{
    
    }
  }
}
</script>
