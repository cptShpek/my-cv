<template>
    <div>
        <h3>{{ job.position }}</h3>
        <p><u>{{ job.time }}</u></p>
        <h4>{{ job.company }}</h4>
        <ul>
            <li v-for="responsibilitie of job.responsibilities" :key="responsibilitie">{{ responsibilitie }}</li>
        </ul>
    </div>
</template>

<script>

    export default {
        name: "MyJobs",
        props:{
            job: Object
        }
    }

</script>

<style scoped>

</style>