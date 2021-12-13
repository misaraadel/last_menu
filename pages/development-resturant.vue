<template>
<div>
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-development />
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('تطوير المطاعم')
</script>