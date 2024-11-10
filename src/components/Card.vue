<script>
    export default {
        props: ['producto'],
        
    }
</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">{{producto.nombre}}</h5>
            <p class="card-text">{{producto.descripcion}}</p>
            <a href="#" class="btn btn-primary">Comprar</a>
        </div>
    </div>
</template>

<style scoped>
    .card {
        max-width: 20rem;
    }       
    .card-title {
        font-size: 1.5rem;
    }
    .card-text {
        font-size: 1.2rem;
    }
    .card-body {
        padding: 1rem;
    }
</style>