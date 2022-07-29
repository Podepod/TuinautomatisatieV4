<template>
  <b-list-group class="mb-1">
    <Lamp v-for="i in 7" :nummer="i" stand="manueel" />    
    <PwmRange />
  </b-list-group>
</template>