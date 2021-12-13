<template>
<div>
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-operating />
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('تشغيل المطاعم')
</script>