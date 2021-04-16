<template>
  <div>
    <v-btn
      :color="color"
      class="button no-text-transform"
      @click="clicked()"
      dark
      :block="block"
    >
      <v-icon v-if="icon" class="icon"> {{ icon }} </v-icon>
      {{ name }}
    </v-btn>
  </div>
</template>
<script>
export default {
  props: ['name', 'icon', 'color', 'block'],
  methods: {
    clicked() {
      this.$emit('clicked')
    },
  },
}
</script>




<style>
.button {
  background-color: #f22539;
  border-radius: 60px;
}
.icon {
  margin: 0 5px 0 5px;
}
</style>