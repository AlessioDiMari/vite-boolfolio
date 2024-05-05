<script>

export default{

    name: 'ProjectCard',

    data(){
        return{

        }
    },

    props : {

        project: Object,

    }
}

</script>

<template>
    
    <div class="card pt-3 px-3 border-0">
        <div class="image">
            <img :src="'http://localhost:8000/storage/' + project.preview" class="card-img-top" alt="...">
        </div>
        <div class="card-body">
            <h5 class="card-title text-center py-3">{{ project.name }}</h5>
            <div class="button d-flex justify-content-center pb-3">
                <router-link :to="{name: 'show-project', params: {slug: project.slug}}" class="btn btn-primary ">Visualizza</router-link>
            </div>
        </div>
    </div>
    
</template>

<style lang="scss">
    .card {
        aspect-ratio: 3 / 2;
        max-width: 600px;

        background: rgb(7,25,82);
        background: radial-gradient(circle, rgba(53,162,159,1) 0%, rgba(11,102,106,1) 35%, rgba(7,25,82,1) 100%);
    }

    .image {
        // width: 100%;
        // height: 300px;
        display: flex; 
    }

    img {
        object-fit: cover;
    }
</style>