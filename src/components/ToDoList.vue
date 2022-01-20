<template>
    <div class="list-items">
        <ToDo  v-for="item in dataList" :key="item.text" :textContent="item.text" :done="item.done" />
    </div>
</template>

<script>
import ToDo from "./ToDo.vue";
export default {
    props: {
        dataList: Array
    },
    components: {
        ToDo
    }
}
</script>
<style lang="scss" scoped>

</style>