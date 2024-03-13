<template>
  <q-card class="my-card">
    <q-card-section class="bg-primary text-white">
      <div class="text-h6">Our Changing Planet</div>
      <div class="text-subtitle2">by John Doe</div>
    </q-card-section>

    <q-separator />

    <q-card-actions align="right">
      <q-btn flat>
        <slot name="action1" message="this is slot message"></slot>
      </q-btn>
      <q-btn flat>
         <slot name="action2"></slot>
      </q-btn>
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  // name: 'ComponentName',
  setup () {
    return {}
  }
}
</script>
