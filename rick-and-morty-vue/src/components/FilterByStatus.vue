<template>
    <div class="filter">
        <div class="item" @click="filter('')">
            ⬜️ All
        </div>
        <div class="item" @click="filter('Alive')">
            🟩 Alive
        </div>
        <div class="item" @click="filter('Dead')">
            🟥 Dead
        </div>
        <div class="item" @click="filter('unknown')">
            🟦 Unknown
        </div>
    </div>
</template>

<script>
import { useStore } from 'vuex';

export default {
    setup() {
        const store = useStore();

        const filter = (status) => {
            store.dispatch('filterByStatus', status);
        };

        return {
            filter,
        };
    },
};
</script>

<style lang="scss">
.filter {
    max-width: 500px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    border-radius: 30px;
    overflow: hidden;
}

.item {
    padding: 1.3rem 0.5rem;
    background-color: var(--background-card);
    text-align: center;
    cursor: pointer;
}

.item:hover {
    color: var(--text-orange);
}
</style>
