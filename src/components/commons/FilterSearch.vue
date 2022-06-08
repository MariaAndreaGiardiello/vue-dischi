<template>
    <div>
        <form class="my-3" @submit.prevent="$emit('searching', searchText)">
            <div class="input-group">
                <input type="text" class="form-control" placeholder="Search by musical genre" aria-label="Recipient's username" aria-describedby="basic-addon2" v-model="searchText">
                <div class="input-group-append">
                    <button class="btn btn-outline-secondary" type="button">Search</button>
                    <button class="btn btn-outline-secondary" type="button">Reset</button>
                </div>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    name: 'FilterSearch',
    data() {
        return {
            searchText: '',
        };
    }
}
</script>

<style lang="scss" scoped>

</style>