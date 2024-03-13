<template>
  <q-page padding>
    <!-- content -->
    <test-slot>
      <template #action2>
         <p class="text-red "> this is 2nd action</p>
      </template>
      <template  #action1="slotProps">
            {{slotProps.message}}
      </template>
    </test-slot>
  </q-page>
</template>

<script>
import Slot from 'src/components/Slot.vue';
export default {
  // name: 'PageName',
  components: {
    TestSlot:Slot
  }
}
</script>
