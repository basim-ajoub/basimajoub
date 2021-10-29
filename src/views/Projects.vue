<template>
    <div class="projects-view">
        
<AllProjects />
    </div>
</template>
<script>
import AllProjects from "../components/projects/showAllProjects.vue"
export default {
    name:"projectsView",
    components:{
        AllProjects,
    },
}
</script>
<style lang="scss">
.projects-view{
    width: 100%;
    height: 100%;
    h1{
        text-align: left;
    }
}
</style>