<template>

    <div>
        
        <button @click="i = !i"><h3>Main Skills</h3></button>
        <button @click="i = !i"><h3>Personal Skills</h3></button>
        <mySkill v-bind:class="info" v-if="i" v-bind:skills="skills.main" :key="a"></mySkill>
        <mySkill v-bind:class="info" v-else v-bind:skills="skills.personal" :key="b"></mySkill>

    </div>

</template>

<script>

import mySkill from "./helpers/skillTab.vue"

export default {

    name:"Summary",

    components: {
        mySkill
    },

    props:{
        skills: Object
    },

    data() {
        return{
            i: true,
            info: "info",
            a: "a",
            b:"b"
        }
    }

}

</script>

<style>
    .info{
        height: 200px;
    }

    .tab-enter-active, .tab-leave-active {
    transition: opacity .5s;
    }
    .tab-enter, .tab-leave-to {
    opacity: 0;
    }

</style>