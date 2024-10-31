<script>
import { NuxtLink } from '#build/components';
</script>

<template>
    <section>
        <div class="container m-auto py-6 px-6">
            <NuxtLink
                to="/jobs"
                class="text-green-500 hover:text-green-600 flex items-center"
            >
            <i class="pi pi-arrow-circle-left mr-3"></i> Back to job listings
            </NuxtLink>
        </div>
    </section>
</template>