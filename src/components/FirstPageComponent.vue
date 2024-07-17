<!--  old approach with defineProps and defineEmits -->
<!-- <template>
    <h2>
        First Page Component
    </h2>
    <button @click="update">Update</button>
    <div>
        Salary in Child Component is : {{ salary }}
    </div>
</template>

<script setup lang="ts">
    defineProps(['salary'])

    const emits = defineEmits(['update'])

    function update(){
        emits('update')
    }
</script> -->
<!-- old approach upto above -->


<!-- new approad using component v-model from below -->
<template>
    <h2>
        First Page Component
    </h2>
    <button @click="update">Update</button>
    <div>
        Salary in Child is : {{ model }}
    </div>
</template>

<script setup lang="ts">
    const model:any = defineModel()

    function update(){
        model.value++
    }
</script>
<!-- new approach upto above -->