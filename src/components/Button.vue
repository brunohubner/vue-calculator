<template>
    <button
        type="button"
        class="button"
        :class="{ double, triple, operation }"
        @click="$emit('onClick', label)"
    >
        {{ label }}
    </button>
</template>

<script>
export default {
    props: {
        label: {},
        operation: { type: Boolean },
        double: { type: Boolean },
        triple: { type: Boolean }
    }
}
</script>

<style>
:root {
    --bg-button: #f0f0f0;
    --border-button: solid 1px #888;
}

.button {
    font-size: 1.4em;
    background-color: var(--bg-button);
    border: none;
    border-right: var(--border-button);
    border-bottom: var(--border-button);
    outline: none;
    font-weight: 600;
    color: #222;
}

.button:active {
    background-color: #ccc;
}

.button.double {
    grid-column: span 2;
}

.button.triple {
    grid-column: span 3;
}

.button.operation {
    background-color: #1e8449;
    color: #fff;
}

.button.operation:active {
    background-color: #1e8449cc;
}
</style>
