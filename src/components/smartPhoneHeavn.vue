<template>
<div :class="$q-screen-gt-lg ? 'container':'q-px-xl' ">
    <div class="row q-col-gutter-lg">
        <div class="col-12">
            <div class="text-h5">{{smartObj.title}}</div>
        </div>
        <div class="col-xs-12 col-sm-6 col-md-5"> 
            <q-img :src="smartObj.img1" width="100%" height="100%" fit="fill" class="rounded-borders" />  
        </div>
        <div class="col-xs-12 col-sm-6 col-md-7">
            <div class="row q-col-gutter-lg">
                <div class="col-xs-12 col-md-6">
                    <q-img :src="smartObj.img2" width="100%"  :ratio="16/8" fit="fill" class="rounded-borders" />
                </div>
                <div class="col-xs-12 col-md-6">
                    <q-img :src="smartObj.img3" width="100%" :ratio="16/8"  fit="fill" class="rounded-borders"/>
                </div>
                <div class="col-xs-12 col-md-6">
                    <q-img :src="smartObj.img4" width="100%" :ratio="16/8"  fit="fill" class="rounded-borders"/>
                </div>
                <div class="col-xs-12 col-md-6">
                    <q-img :src="smartObj.img5" width="100%" :ratio="16/8"  fit="fill" class="rounded-borders"/>
                </div> 
            </div>
        </div> 
    </div>
</div>
<!-- <smartPhoneHeaven/> -->
</template> 
<script>
export default {  
    data() {
        return {
          
        }
    }, 
    props:{
      smartObj:Object
  }

}
</script>

<style scoped>
q-img{
  max-width: 100%;
  max-height: 100%;
}
</style>
