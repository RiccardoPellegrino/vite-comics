<template>
    <div class="list">
        <h4>{{ obj.title }}</h4>
        <div>
            <ul>
                <li v-for="(link, index) in obj.links" :key="index">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>

        </div>
    </div>
</template>

<script>
export default {
    name: 'DcComponent',
    props: [
        'obj'
    ]
}
</script>

<style lang="scss" scoped>

</style>