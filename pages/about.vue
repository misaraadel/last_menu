<template>
<div>
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-about/>

    <home-about-content />
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('عن المنيو')
</script>