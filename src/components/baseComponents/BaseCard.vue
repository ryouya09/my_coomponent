<template>
    <div class="card-wrapper" :style="styles">
        <a :href="urlPath">
            <div class="card">
                <img :src="imgPath" :alt="cardAlt" />
                <p>{{ cardDiscription }}</p>
            </div>
            {{ linkName }}
        </a>
    </div>
</template>

<script lang="ts">
import { computed, defineComponent, PropType } from 'vue'

export default defineComponent({
    props: {
        urlPath: {
            type: String as PropType<string>,
        },
        imgPath: {
            type: String as PropType<string>,
        },
        cardAlt: {
            type: String as PropType<string>,
        },
        cardDiscription: {
            type: String as PropType<string>,
        },
        linkName: {
            type: String as PropType<string>,
        },
        cardWidth: {
            type: String as PropType<string>,
            default: 'auto'
        }
    },
    setup(props) {
        const styles = computed(() => ({
            '--card-width': props.cardWidth
        }))
        return {
            styles
        }
    }
})
</script>
<style scoped>
img{
    width: var(--card-width);
}
</style>
