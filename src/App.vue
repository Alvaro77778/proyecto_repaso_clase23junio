<template>
    <div class="container">
      <div class="row">
        <div class="col-md-8">
            <ComponenteCarroCompras
            v-bind:productos="datosPolera"
            />
        </div>
        <div class="col-md-4">
            <ComponentePagoCompras/>
        </div>
      </div>
    </div>

    
    


  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ComponenteCarroCompras from './components/ComponenteCarroCompras.vue';
import ComponentePagoCompras from './components/ComponentePagoCompras.vue';
export default {
  name: 'App',
  components: {
    HelloWorld,
    ComponenteCarroCompras,
    ComponentePagoCompras
},
data: function(){
  return{
    datosPolera: [
      {
        rutaPolera: 'https://falabella.scene7.com/is/image/Falabella/15378577_1?wid=1500&hei=1500&qlt=70',
        tituloPolera: 'Polera',
        descripcionPolera: 'color negro',
        costoPolera: '12000'
      },
      {
        rutaPolera: 'https://falabella.scene7.com/is/image/Falabella/15378573_1?wid=1500&hei=1500&qlt=70',
        tituloPolera: 'Polera',
        descripcionPolera: 'color blanco',
        costoPolera: '12000'
      },
      {
        rutaPolera: 'https://falabella.scene7.com/is/image/Falabella/gsc_119230213_2225617_1?wid=1500&hei=1500&qlt=70',
        tituloPolera: 'Polera',
        descripcionPolera: 'color morado',
        costoPolera: '16990'
      }
    ]
  }
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
