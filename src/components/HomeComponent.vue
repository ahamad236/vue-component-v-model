<!-- old approach with defineProps and defineEmits -->
<!-- <template>
    <h1>
        Home Component
    </h1>
    <div>
        Salary in Parent Component is : {{ Salary }}
    </div>
    <FirstPage :salary="Salary" @update="update"></FirstPage>
</template>

<script setup lang="ts">
    import FirstPage from './FirstPageComponent.vue'
    import { ref } from 'vue'

    const Salary = ref(28000)

    function update(){
        Salary.value++
    }
</script> -->
<!-- old approach upto above -->


<!-- new approad using component v-model from below -->
<template>
    <h1>
        Home Component
    </h1>
    <div>
        Salary in Home is : {{ salary }}
    </div>
    <FirstPage v-model="salary"></FirstPage>
</template>

<script setup lang="ts">
    import FirstPage from "./FirstPageComponent.vue"
    import { ref } from "vue"

    const salary = ref<number>(28000)
</script>
<!-- new approach upto above -->