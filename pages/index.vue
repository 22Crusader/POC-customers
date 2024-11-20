<template>
    <div class="customers">
        <div class="customers__header">
            <span>
                Searchbar
            </span>
            <span>
                Filter1
            </span>
            <span>
                Filter2
            </span>
            <span>
                Filter3
            </span>
        </div>
        <div class="customers__list">
            <nuxt-link
                v-for="org in 5"
                class="customers__list-item"
                :to="`/customers/details/${org}`"
                :key="org"
            >
                Organization {{ org }}
            </nuxt-link>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
    .customers {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        width: 100%;
        padding: 0 2rem;

        &__header {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        &__list {
            display: flex;
            flex-direction: column;
            flex-grow: 1;
            gap: 1rem;
        }

        &__list-item {
            font-size: 1.25rem;
            font-weight: 500;
        }
    }
</style>
