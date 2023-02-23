<script setup>
import GuestLayout from '@/Layouts/GuestLayout.vue'
import Label  from '@/Components/InputLabel.vue'
import Input from '@/Components/TextInput.vue'

const emitTest = e => console.log(e);

</script>

<template>
<GuestLayout>
  何かを書く
  <Label>

  </Label>
  <Input
  modelValue="初期値が入ります"
  @update:modelValue="emitTest"
  >
</Input>
</GuestLayout>

</template>