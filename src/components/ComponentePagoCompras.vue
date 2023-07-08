<template>
    <div id="componentePagoCompras">
        <h3>Componente Pago Compras</h3>
        <p>RESUMEN COMPRA</p>
        <hr>
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <p>Cantidad</p>
                </div>
                <div class="col-md-6">
                    <p>Valor</p>
                </div>
            </div>
        </div>
        <hr>
        <label for="envios">Envio</label>
        <select name="envios" id="envios">
            <option value="express"> Envio express 5.000</option>
            <option value="normal"> Envio normal 3.000</option>
            <option value="overnight"> Envio overnight 10.000</option>
        </select>       
        <hr>
        <label for="descuentos">Codigo de descuentos</label>
        <input type="text" id="descuentos" placeholder="Ingresa tu codigo">
        <hr>
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <p>Precio total</p>
                </div>
                <div class="col-md-6">
                    <p>Precio</p>
                </div>
            </div>
        </div>
        <div>
            <button class="btn btn-danger">
                Realizar compra
            </button>
        </div>
    </div>
</template>

<script>

    export default{
        name: 'componentePagoCompras',
      
        data: function(){
            return{

            }
        },
        methods: {

        }
    }
</script>
<style scoped>
    #componentePagoCompras{
        background-color: aquamarine;
    }
</style>