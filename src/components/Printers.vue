<template>
  <v-select
      label="Printer"
      v-model="sel"
      :items="list"
      item-value="id"
      item-text="name"
      @input="changePrinter()"
      required
    ></v-select>
</template>

<script>
  export default {
    data: function(){
      return {
        sel: 1
      }
    },
    props: ['list','selected'],
    watch: {
      selected: function(){
        console.log("watch");
        this.sel = this.selected;
      }
    },  
    methods: {
      changePrinter: function(){
        console.log("child changed: " + this.sel);
        this.$emit('change',this.sel);
      }
    }
  }
</script>
