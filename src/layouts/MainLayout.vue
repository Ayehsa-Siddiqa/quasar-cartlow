<template>
<q-layout view="lHh Lpr lFf">
    <!-- :class="$q.screen.lt.md ? 'bg-red' : $q.screen.lt.sm ? 'bg-blue' : $q.screen.gt.md ? 'bg-yellow' : 'bg-green'" -->
    <q-header elevated class="text-black bg-white" :class="$q.screen.gt.lg ? 'container' : 'q-px-lg'">
        <navbar />
        <q-toolbar>
            <div class="row full-width">
                <div class="col-2">
                    <q-btn flat dense round icon="menu" @click="toggleLeftDrawer" label="All Categories" />
                </div>
                <div class="col-10">
                    <q-tabs outside-arrows>
                        <q-tab name="60%-off" label="60% off" />
                        <q-tab name="MOBILES" label="MOBILES" />
                        <q-tab name="LAPTOPS" label="LAPTOPS" />
                        <q-tab name="TABLETS" label="TABLETS" />
                        <q-tab name="smartwatches" label="smartwaches" />
                        <q-tab name="fragrences" label="fragrences" />
                        <q-tab name="watches" label="watches" />
                        <q-tab name="fashion" label="fashion" />
                        <q-tab name="small appliance" label="small appliance" />
                        <q-tab name="sell your old devices" label="cell you old devices" />
                        <q-tab name="videos" label="Videos" />
                        <q-tab name="articles" label="Articles" />
                    </q-tabs>
                </div>
            </div> 
        </q-toolbar>
    </q-header>
<!-- 
    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
        <q-list>
            <q-item-label header>
                Essential Links
            </q-item-label> 
            <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
        </q-list>
    </q-drawer> -->

    <q-page-container>
        <router-view />
    </q-page-container>
</q-layout>
</template>

<script>
import {
    defineComponent,
    ref
} from 'vue'
import EssentialLink from 'components/EssentialLink.vue'
import navbar from 'src/components/navbar.vue';

const linksList = [{
        title: 'Docs',
        caption: 'quasar.dev',
        icon: 'school',
        link: 'https://quasar.dev'
    },
    {
        title: 'Github',
        caption: 'github.com/quasarframework',
        icon: 'code',
        link: 'https://github.com/quasarframework'
    },
    {
        title: 'Discord Chat Channel',
        caption: 'chat.quasar.dev',
        icon: 'chat',
        link: 'https://chat.quasar.dev'
    },
    {
        title: 'Forum',
        caption: 'forum.quasar.dev',
        icon: 'record_voice_over',
        link: 'https://forum.quasar.dev'
    },
    {
        title: 'Twitter',
        caption: '@quasarframework',
        icon: 'rss_feed',
        link: 'https://twitter.quasar.dev'
    },
    {
        title: 'Facebook',
        caption: '@QuasarFramework',
        icon: 'public',
        link: 'https://facebook.quasar.dev'
    },
    {
        title: 'Quasar Awesome',
        caption: 'Community Quasar projects',
        icon: 'favorite',
        link: 'https://awesome.quasar.dev'
    }
]

export default defineComponent({
    name: 'MainLayout',

    components: {
        EssentialLink,
        navbar
    },

    setup() {
        const leftDrawerOpen = ref(false)

        return {
            essentialLinks: linksList,
            leftDrawerOpen,
            toggleLeftDrawer() {
                leftDrawerOpen.value = !leftDrawerOpen.value
            }
        }
    }
})
</script>
