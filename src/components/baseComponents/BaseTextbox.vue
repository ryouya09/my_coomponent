<template>
    <div class="textbox-wrapper">
        <input
            type="text"
            class="textbox"
            :value="text"
            :placeholder="placeName"
            @input="$emit('update:text', $event.target.value)"
        />
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
    props:{
        text:{
            type: String as PropType<string>,
        },
        placeName:{
            type: String as PropType<string>
        },
    }, 
})
</script>

<style  scoped>
    .textbox{
        border: 1px solid black
    }
</style>