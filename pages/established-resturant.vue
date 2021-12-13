<template>
<div>
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-established />
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('تأسيس المطاعم')
</script>