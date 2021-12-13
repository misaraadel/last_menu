<template>
<div class="heading-data">
    <h4 :class="`${headingStyle} text-heading font-bold`">
        {{ headContent }}
    </h4>

    <p :class="`${descriptionStyle} font-normal leading-paragraph`">
        {{ description }}
    </p>
</div>
</template>

<script setup lang="ts">
    defineProps({
        headContent: String,
        headingStyle: String,
        description: String,
        descriptionStyle: String
    })
</script>