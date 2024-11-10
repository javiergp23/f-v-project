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