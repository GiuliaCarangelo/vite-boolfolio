<script>
import axios from 'axios';

export default {
    name: 'ProjectList',
    data(){
        return{
            projects: [],
        }
    },
    methods:{
        getProjects(){
            axios.get('http://127.0.0.1:8000/api/projects', {
                params: {
                }
            })
            .then((response) => {
                console.log(response.data.results.data);
                this.projects = response.data.results.data;

            })
        }
    }
}
</script>