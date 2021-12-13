<template>
<div>
    <coreSub-header :subHeading="`${aboutSubHeading}`"/>

    <home-contact/>
</div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const aboutSubHeading = ref('طلب الخدمة')
</script>