<script>
export default {
    data() {
        return {
            numero1: 0,
            numero2: 0,
            resultado: 0
        }
    },
    methods: {
        sumar() {
            this.resultado = parseInt(this.numero1) + parseInt(this.numero2);
        },
        resta() {
            this.resultado = parseInt(this.numero1) - parseInt(this.numero2);
        },
        mul() {
            this.resultado = parseInt(this.numero1) * parseInt(this.numero2);
        },
        div() {
            this.resultado = parseInt(this.numero1) / parseInt(this.numero2);
        }
    }
}
</script>

<template>
    <div class="container mt-5 d-flex justify-content-center">
        <div class="calculator">
            <div class="display">{{ resultado }}</div>
            <h1 class="text-center">Calculadora</h1>
            <div class="input-group">
                <label>Numero 1</label>
                <input type="number" v-model="numero1">                
            </div>
            <div class="input-group">
                <label>Numero 2</label>
                <input type="number" v-model="numero2">                
            </div>
            <div class="buttons">
                <button @click="sumar" class="btn">+</button>
                <button @click="resta" class="btn">-</button>
                <button @click="mul" class="btn">×</button>
                <button @click="div" class="btn">÷</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, #2c3e50, #4ca1af);
}

.calculator {
    width: 300px;
    padding: 20px;
    border-radius: 10px;
    background: #222;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    text-align: center;
    color: white;
    position: relative;
}

.display {
    width: 100%;
    height: 50px;
    background: #000;
    color: #0f0;
    font-size: 24px;
    text-align: right;
    padding: 10px;
    border-radius: 5px;
    margin-bottom: 15px;
}

h1 {
    font-size: 20px;
    margin-bottom: 15px;
}

.input-group {
    margin-bottom: 15px;
    display: flex;
    flex-direction: column;
    text-align: left;
}

.input-group label {
    font-size: 14px;
    margin-bottom: 5px;
    color: #ccc;
}

.input-group input {
    padding: 8px;
    border: none;
    border-radius: 5px;
    background: #333;
    color: white;
    font-size: 16px;
    text-align: center;
}

.buttons {
    display: flex;
    justify-content: space-between;
    margin-top: 10px;
}

.btn {
    width: 45px;
    height: 45px;
    border: none;
    border-radius: 5px;
    background: #ff9500;
    color: white;
    font-size: 18px;
    cursor: pointer;
    transition: 0.3s;
}

.btn:hover {
    background: #e08e00;
}
</style>
