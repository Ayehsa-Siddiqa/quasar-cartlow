<template>
<div :class="$q.screen.gt.lg? 'container' : 'q-px-lg' " class="q-pt-lg">
    <div class="text-h5 q-py-sm">{{commonObj3.title}}</div>
    <div class="row q-col-gutter-lg">
        <div class="col-xs-12 col-md-5">
            <q-img :src="commonObj3.img1" width="100%" height="92.5%" class="rounded-borders" />
        </div>
        <div class="col-xs-12 col-md-7">
            <div class="row q-col-gutter-xs">
                <div class="col-12">
                    <q-img :src="commonObj3.img2" width="100%" height="93%" class="rounded-borders" :fit="fill" /> 
                </div>
                <div class="col-12">
                  <q-img :src="commonObj3.img3" width="100%" height="93%" class="rounded-borders" :fit="fill" /> 
              </div>
            </div>
        </div>

    </div>
</div>
</template>

<script>
export default {
    // name: 'ComponentName',
    setup() {
        return {}
    },
    props: {
        commonObj3: Object,
    }
}
</script>
