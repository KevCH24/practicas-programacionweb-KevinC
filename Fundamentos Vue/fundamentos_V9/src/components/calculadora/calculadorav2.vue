<script>
export default{
    data() {
        return {
            display: '', 
            currentValue: 0,
            operator: null,
        }
    },
    methods: {
        agregarNumero(numero) {
            this.display += numero;
        },
        calcular() {
            try {
                this.currentValue = eval(this.display);
                this.display = this.currentValue.toString();
            } catch (error) {
                this.display = 'Error'; 
            }            
        },
        limpiarDisplay() {
            this.display = '';
        },
        eliminarNumero() {
            this.display = this.display.slice(0, -1);
        },
        limpiarUltimaEntrada() {
            this.display = this.display.slice(0, -1);
        },
        agregarOperador(operador) {
            if (this.display && !['+', '-', '*', '/'].includes(this.display[this.display.length - 1])) {
                this.display += operador;
            }
        },
        agregarPunto() {
            if (!this.display.includes('.')) {
                this.display += '.';
            }
        },
        igual() {
            this.calcular();
        },
        calcularPorcentaje() {
            if (this.display) {
                // Si hay un número en la pantalla, calcula el porcentaje de ese número
                this.display = (parseFloat(this.display) / 100).toString();
            }
        }
    },
}
</script>

<template>
    <div class="container d-flex justify-content-center mt-4" style="height: 400px;">
        <div class="card p-3" style="width: 300px; background-color: black">
            <div class="card-body"> 
                <h3 class="text-center" style="color: white;">Calculadora V2</h3>
                <!-- Display de la calculadora -->
                <div class="mb-3">
                    <input type="text" class="form-control" v-model="display" disabled>
                </div>
                <!-- Botones de la calculadora -->
                <div class="d-flex justify-content-between">
                    <button class="btn btn-secondary" @click="limpiarDisplay">C</button>
                    <button class="btn btn-secondary" @click="limpiarUltimaEntrada">CE</button>
                    <button class="btn btn-danger" @click="eliminarNumero">&#9003;</button>
                    <button class="btn btn-secondary" @click="calcularPorcentaje">%</button>
                </div>
                <div class="d-flex justify-content-between mt-2">
                    <button class="btn btn-secondary" @click="agregarNumero(7)">7</button>
                    <button class="btn btn-secondary" @click="agregarNumero(8)">8</button>
                    <button class="btn btn-secondary" @click="agregarNumero(9)">9</button>
                    <button class="btn btn-danger" @click="agregarOperador('/')">/</button>
                </div>
                <div class="d-flex justify-content-between mt-2">
                    <button class="btn btn-secondary" @click="agregarNumero(4)">4</button>
                    <button class="btn btn-secondary" @click="agregarNumero(5)">5</button>
                    <button class="btn btn-secondary" @click="agregarNumero(6)">6</button>
                    <button class="btn btn-danger" @click="agregarOperador('*')">x</button>
                </div>
                <div class="d-flex justify-content-between mt-2">
                    <button class="btn btn-secondary" @click="agregarNumero(1)">1</button>
                    <button class="btn btn-secondary" @click="agregarNumero(2)">2</button>
                    <button class="btn btn-secondary" @click="agregarNumero(3)">3</button>
                    <button class="btn btn-danger" @click="agregarOperador('-')">-</button>
                </div>
                <div class="d-flex justify-content-between mt-2">
                    <button class="btn btn-secondary" @click="igual">=</button>
                    <button class="btn btn-secondary" @click="agregarNumero(0)">0</button>
                    <button class="btn btn-secondary" @click="agregarPunto">.</button>
                    <button class="btn btn-danger" @click="agregarOperador('+')">+</button>
                </div>
            </div>
        </div>
    </div>
</template>
