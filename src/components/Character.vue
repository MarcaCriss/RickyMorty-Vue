<template>
    <div class="column is-12-mobile is-4-desktop is-4-tablet">
        <div class="card">
            <div class="card-header">
                <img v-bind:src="character.image" alt="">
            </div>
            <div class="content">
                <h3 class="title is-size-4">{{ character.name }}</h3>
                <button class="button is-success is-rounded is-small" @click="showMore(character.id)">Ver mas</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ["character"],
        data() {
            return {

            }
        },
        methods: {
            showMore(id) {
                this.$emit('showModal', id);
            }
        },
        created() {

        }
        
    }
</script>

<style lang="scss" scoped>

</style>