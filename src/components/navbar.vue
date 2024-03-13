<template>
    <!-- :class="$q.screen.gt.lg ? 'container' : 'q-px-lg'" -->
<div>
    <div class="row q-pt-md q-col-gutter-lg">
        <div class="col-xs-2">
            <img src="public/images/logo/logo-cartlow.svg" width="140px" class="q-pl-md">
        </div>
        <div class="col-xs-12 col-sm-10 col-md-6">
            <q-input class="full-width" color="grey-10" dense  outlined v-model="text">
                <template v-slot:append>
                    <q-btn color="grey-10" class="search-btn q-py-sm">
                        <q-icon name="search" />
                    </q-btn>
                </template>
            </q-input>
        </div>
        <div class="col-xs-12 col-md-4">
            <q-btn-dropdown icon="img:public/images/logo/uae-flag.png" @mouseover="open = true" @mouseleave="open = false" flat dense label="UAE" v-model="open">
                <q-list>
                    <q-item clickable v-close-popup>
                        <q-item-section avatar>
                            <img src="public/images/logo/uae-flag.png">
                        </q-item-section>
                        <q-item-section>
                            <q-item-label>UAE</q-item-label>
                        </q-item-section>
                    </q-item>
                    <q-item clickable v-close-popup>
                        <q-item-section avatar>
                            <img src="public/images/logo/uae-flag.png">
                        </q-item-section>
                        <q-item-section>
                            <q-item-label>UKS</q-item-label>
                        </q-item-section>
                    </q-item>
                    <q-item clickable v-close-popup>
                        <q-item-section avatar>
                            <img src="public/images/logo/uae-flag.png">
                        </q-item-section>
                        <q-item-section>
                            <q-item-label>UKS</q-item-label>
                        </q-item-section>
                    </q-item>
                </q-list>
            </q-btn-dropdown>
            <q-btn @click="showLoading" dense :ripple="false" class="btn--no-hover" :loading="isLoading" flat label="Arabia123" icon="flag" />
            <q-btn flat  icon="factory" label="Cart" />
            <q-btn flat dense text-color="black" icon="person" label="Sign In" />
        </div>
    </div>
</div>
</template>

<script>
export default {
    // name: 'ComponentName',
   
    data() {
        return {
            open: false,
            isLoading: false
        }
    },

    methods: {
        showLoading() {
            this.isLoading = true;
            setTimeout(() => {
                this.isLoading = false;
            }, 500);
        }
    }
   
}
</script>

<style scoped>
.search-btn {
    margin-right: -12px;
}
</style>
