<template>
    <header>
        <h1>{{ title }}</h1>
        <Button 
            @btn-click="$emit('toggle-add-task')" 
            :text="showAddTask ? 'Close' : 'Add Task'" 
            :color="showAddTask ? 'red' : 'green'" 
        />
    </header>
</template>

<script>

import Button from './Button'

export default {
    name: 'Header',
    components: {
        Button,
    },
    props: {
        title: String,
        showAddTask: Boolean
    }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-content: center;
    margin-bottom: 20px;
}
</style>