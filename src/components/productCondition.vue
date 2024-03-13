<template>
<div class="q-px-lg">
    <div class="justify q-py-xs">
        <span class="text-h6 q-mr-auto">Our products condition</span>
        <q-btn flat icon-right="keyboard_double_arrow_right" label="see all" no-caps href="https://quasar.dev/vue-components/button#progress-related" />
    </div>
    <div class="row q-col-gutter-lg">
        <div class="col-12 col-sm-6 col-md-3" v-for="data in productCondition" :key="data">
            <q-card dark bordered class="bg-white text-black q-pa-md preLoved">
                <q-card-section>
                    <div class="text-h6">{{data.title}}</div>
                </q-card-section>
                <q-separator class="seprator" grey-13 />
                <div class="text-subtitle2 q-py-xs">{{data.upTo}}</div>
                <div>
                    <span class="fs-25 text-green text-weight-bold">{{data.percent}}</span><span>{{data.percentLess}}</span>
                </div>
                <div class="q-pt-xs text-weight-light fs-13">
                    <q-icon name="task_alt" class="q-pr-xs" />{{data.desc1}}
                </div>
                <div class="q-pt-xs text-weight-light fs-13">
                    <q-icon name="task_alt" class="q-pr-xs" />{{data.desc2}}
                </div>
                <div class="q-pt-xs text-weight-light fs-13">
                    <q-icon name="task_alt" class="q-pr-xs" />{{data.desc3}}
                </div>
                <div class="bg-grey-3 highlight q-pa-sm fs-13 q-my-md">
                    {{data.highlight}}
                </div>
                <q-btn flat style="border:1px solid black; width:100%" label="See Products" class="preCardBtn" />
            </q-card>
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
        productCondition: Array
    }
}
</script>

<style scoped>
.preLoved:hover {
    background-color: rgb(29, 47, 66) !important;
    color: white !important;
}

.preLoved:hover .seprator {
    background-color: white !important;
}

.preLoved:hover .preCardBtn {
    background-color: white !important;
    border-color: white !important;
    color: black;
}

.highlight {
    border-radius: 7px !important;
}

.preLoved:hover .highlight {
    background-color: rgb(46, 62, 80) !important;
}

.justify {
    display: flex;
    justify-content: space-between;
}
</style>
