<template>

    <div id="componenteCarroCompras">
        <h3>Componente Carro compras</h3>
        <div class="card mb-3" v-for="(producto, index) in productos" v-bind:key="index">
            <div class="row g-0">
                <div class="col-md-4">
                    <div class="container">
                        <div class="row">
                            <div class="col-md-6">
                                <img v-bind:src="producto.rutaPolera" class="img-fluid rounded-start tamañoImagen" alt="...">
                            </div>
                            <div class="col-md-6">
                                <p>
                                    {{ producto.tituloPolera }}
                                </p>
                                <p>
                                    {{ producto.descripcionPolera }}
                                </p>
                            </div>
                        </div>
                    </div>
                    
                </div>
                <div class="col-md-4">
                        <div class="container">
                            <div class="row">
                                <div class="col-md-4">
                                    <button v-on:click.prevent="aumentar(index)">+</button>
                                </div>
                                <div class="col-md-4">
                                    <input type="text" size="1" v-model="cantidadProducto[index]">
                                </div>
                                <div class="col-md-4">
                                    <button v-on:click.prevent="disminuir(index)">-</button>
                                </div>
                            </div>
                        </div>
                 
                       
                        
                    
                </div>
                <div class="col-md-4">
                    <p>{{ producto.costoPolera }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'componenteCarroCompras',
        props:{
            productos:{
                type: Array,
                required: true

            }
        },
        data: function(){
            return{
                cantidadProducto:[
                    0,
                    0,
                    0
                ]
            }
        },
        methods: {
            aumentar: function(indice){
                this.cantidadProducto [indice] += 1;
            },
            disminuir: function(indice){
                if(this.cantidadProducto[indice] > 0 ){
                    this.cantidadProducto [indice] -= 1;
                }
                
            }
        }
    }



</script>

<style scoped>

    #componenteCarroCompras{
        background-color: brown;
        color: wheat;
    }
    .tamañoImagen{
        width: 50%;
    }


</style>