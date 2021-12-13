<template>
<div class="menu-data">
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-menu />
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('منيو المطاعم')
</script>

<style lang="scss">
.menu-data{
    .heading-data{
        display: none;
    }
}
</style>