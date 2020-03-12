<template>
    <div>
        <strong>   
            <ul>
                <li v-for="skill in skills" :key="skill">{{skill}}</li>
            </ul>
        </strong>
    </div>
</template>

<script>
export default {
    name:"mySkill",
    props:{
        skills: Array
    }
}
</script>

