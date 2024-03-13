<template>
<div class="q-pa-md">
    <q-carousel v-model="slide" transition-prev="slide-right" transition-next="slide-left" swipeable animated control-color="black" navigation height="300px" class=" custome-bg rounded-borders q-pb-xl">
        <q-carousel-slide class="column no-wrap" v-for="(slide, index) in 5" :name="index+1" > 
            <div class="row fit justify-start items-center q-gutter-sm q-col-gutter no-wrap">
                <q-card class="beforeIcon rounded-borders col-6 full-height">
                    <div class="row">
                        <div class="col-2">
                            <q-icon name=" feedback" size="50px" class="q-pt-md q-pl-md" color="green" />
                        </div>
                        <div class="col-10">
                            <q-icon name="star" v-for="str in 5" :key="str" color="yellow-13" size="15px" class="q-pt-md" />
                            <div class="text-body1 q-pt-xs q-pb-xl">
                                I bought 2 denon wireless speakers..almost new at a steal price. Its been more than 8 months and its all simply great. Amazing prices, delivery, packing. LOVE IT
                            </div>
                            <div class="text-h6 q-pt-sm">
                                -Timmy Thomas
                            </div>
                        </div>
                    </div> 
                </q-card>
                <q-card class="beforeIcon rounded-borders col-6 full-height">
                  <div class="row">
                      <div class="col-2">
                          <q-icon name=" feedback" size="50px" class="q-pt-md q-pl-md" color="green" />
                      </div>
                      <div class="col-10">
                          <q-icon name="star" v-for="str in 5" :key="str" color="yellow-13" size="15px" class="q-pt-md" />
                          <div class="text-body1 q-pt-xs q-pb-xl">
                              I bought 2 denon wireless speakers..almost new at a steal price. Its been more than 8 months and its all simply great. Amazing prices, delivery, packing. LOVE IT
                          </div>
                          <div class="text-h6 q-pt-sm">
                              -Timmy Thomas
                          </div>
                      </div>
                  </div> 
              </q-card>  
            </div>
        </q-carousel-slide>

    </q-carousel>
</div>
</template>


<script>
export default {
    // name: 'ComponentName',
    data() {
        return {
            slide: 1
        }
    }
}
</script>
<style scoped>
    
   .custome-bg{
    background-color: rgb(242, 242, 242);
   }
</style>
