<template>
  <div>
    <h2>Printers</h2>
    <printers :list="printers" :selected="selected" @change="printerChanged"></printers>
  </div>
</template>

<script>
import Printers from './Printers.vue';

export default {
  data() {
    return {
      printers: [
        {
          name: 'DYMO LabelWriter 450 Turbo',
          id: 1
        },
        {
          name: 'Zebra UPS 2844',
          id: 2
        },
        {
          name: 'CAB MACH4/300',
          id: 3
        }
      ],
      selected: 1
    }
  },
  mounted (){
    let vm = this;
    setInterval(function(){
      console.log("Selecting a different value");
      console.log(vm.printers);
      vm.selected = (vm.selected == vm.printers.length) ? 1 : vm.selected + 1;
    }, 2000);
  },
  methods: {
    printerChanged: function(){
      console.log("Printer changed. Selected ID: ", this.selected);
    }
  },
  components: {
    Printers
  }
}

</script>
