<template>
  <b-list-group>
    <Lamp v-for="i in 7" :nummer="i" stand="manueel" />    
    <PwmRange />
  </b-list-group>
</template>