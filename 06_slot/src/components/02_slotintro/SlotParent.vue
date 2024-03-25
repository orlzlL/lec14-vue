<template>
    <div class="parentContainer">
        <h1>Parent</h1>
        <Child>
            {{  slotData }}
        </Child>
    </div>
</template>

<!-- 
    slot:
    슬롯(slot)은 Vue 컴포넌트에서 컨텐츠를 전달하는 매커니즘으로 부모 컴포넌트에서 자식 컴포넌트로
    데이터나 구조를 전달하는데 사용된다.
    (주로 구조(부모에서 만든 컴포넌트 요소)를 전달하는 데 목적이 있음, 데이터는 prop으로..)
-->
<script setup>
    import Child from "./SlotChild.vue";
    import {ref} from 'vue';

    const slotData = ref('hello Data');
</script>

<style scoped>
    .parentContainer {
        display: flex;
        align-items: center;
        flex-direction: column;
        border: 1px solid black;
    }
</style>