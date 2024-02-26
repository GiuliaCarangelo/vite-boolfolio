<template lang="">
<div class="container mt-5">
    <div class="row">
        <div class="col-3" v-for="project in projects">
            <div class="wrapper card d-flex flex-wrap mb-5" style="width: 18rem;">
                <div class="card-body">
                    <h3 class="card-title">Project Name: {{project.name}}</h3>
                    <p class="card-text" >Programming Languages: {{project.programming_languages}}</p>
                    <a :href=project.repo_url class="btn btn-primary mb-3">GitHub Repository</a>
                    <h4>Created at: {{project.creation_day}}</h4>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import axios from 'axios';
import CardItem from '../components/CardItem.vue';

export default {
    name: 'ProjectList',
    data() {
        return {
            projects: [],
        }
    },
    components: { CardItem },
    methods: {
        getProjects() {
            axios.get('http://127.0.0.1:8000/api/projects', {
                params: {
                }
            })

                .then((response) => {
                    console.log(response.data);
                    this.projects = response.data.result;

                })
        }
    },
    created() {
        this.getProjects();
    }
}
</script>

<style>



.wrapper{
    height: 300px;
}
</style>