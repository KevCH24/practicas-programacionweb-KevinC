<template>
    <div class="container">
        <div class="row mt-4 p-4">
            <div class="evento">
                <h4>Evento Click</h4>
                <button @click="clic" class="btn btn-primary" type="button">Dale clic</button>
                <button @click="soyButon" class="btn btn-success mx-2" type="button">Dale clic</button>
            </div> 

            <div class="evento">
                <h4>Evento Change</h4>
                <label class="input-group-text" for="nombre">Ingresa tu nombre</label>
                <input class="form-control mt-2" type="text" id="nombre" @change="nombreE">
                <p>El nombre ingresado es: <strong> {{ nombre }}</strong> </p>
            </div>

            <div class="evento">
                <h3>Evento de Mouse</h3>
                <div class="mouse-box text-center"
                    :class="{ 'hovered': isHovered }"
                    @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
                    <p>Pase el mouse</p>
                    <p>{{ mensaje }}</p>
                </div>
            </div>
        </div>    
    </div>
</template>

<script>
export default {
    data() {
        return {
            nombre: '',
            mensaje: '',
            isHovered: false
        }
    },
    methods: {
        clic() {
            alert('Gracias por darle clic');
        },
        soyButon() {
            alert('Soy un botón');
        },
        nombreE(event) {  
            this.nombre = event.target.value;
        },
        mostrarMensaje() {
            this.mensaje = 'Mouse dentro del rectángulo';
            this.isHovered = true;
        },
        ocultarMensaje() {
            this.mensaje = 'Mouse fuera del rectángulo';
            this.isHovered = false;
        }
    }
}
</script>

<style>
/* Estilo general */
body, html {
    font-family: 'Poppins', sans-serif;
    background: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

/* Centrado del contenedor */
.container {
    background: linear-gradient(135deg, gray, black);
    padding: 30px;
    border-radius: 15px;
    color: white;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

/* Espaciado entre eventos */
.evento {
    margin-bottom: 20px;
    padding: 15px;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 10px;
    width: 100%;
}

/* Botones estilizados */
.btn {
    font-weight: bold;
    transition: 0.3s ease-in-out;
}

.btn-primary {
    background-color: orange;
    border: none;
}

.btn-primary:hover {
    background-color: #ff4f91;
}

.btn-success {
    background-color: blue;
    border: none;
}

.btn-success:hover {
    background-color: #3aaa3a;
}

/* Caja de evento de mouse con degradado */
.mouse-box {
    width: 300px;
    height: 150px;
    background: linear-gradient(135deg, #000000, #434343);
    text-align: center;
    padding: 15px;
    border-radius: 12px;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    transition: background 0.5s ease-in-out, transform 0.3s;
}

/* Cambia el degradado al pasar el mouse */
.mouse-box.hovered {
    background: linear-gradient(135deg, #ff512f, #dd2476);
    transform: scale(1.05);
}
</style>

