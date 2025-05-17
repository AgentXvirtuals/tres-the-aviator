<script setup lang="ts">
import { TresVector3 } from '@tresjs/core'
import PilotBody from './body.vue'
import PilotFace from './face.vue'
import PilotHairs from './hairs.vue'
import PilotGlass from './glass.vue'
import PilotEar from './ear.vue'

defineProps<{
  position?: TresVector3
}>()
</script>

<template>
  <TresObject3D name="penguin" :position="position">
    <PilotBody />
    <PilotFace />
    <PilotGlass /> <!-- Pico -->
    <PilotEar />   <!-- Alas -->
    <!-- PilotHairs opcional -->
  </TresObject3D>
</template>
