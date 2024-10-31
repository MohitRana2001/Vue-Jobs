<script>
import { useRoute } from 'vue-router';
import logo from '@/public/img/logo.png';

export default {
  data() {
    return {
      logo,
    };
  },
  computed: {
    route() {
      return useRoute();
    },
  },
  methods: {
    isActiveLink(routePath) {
      return this.route.path === routePath;
    },
  },
};
</script>


<template>
  <nav class="bg-green-700 border-b border-green-500">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="flex h-20 items-center justify-between">
        <div
          class="flex flex-1 items-center justify-center md:items-stretch md:justify-start"
        >
          <!-- Logo -->
          <NuxtLink class="flex flex-shrink-0 items-center mr-4" to="/">
            <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
            <span class="hidden md:block text-white text-2xl font-bold ml-2"
              >Vue Jobs</span
            >
          </NuxtLink>
          <div class="md:ml-auto">
            <div class="flex space-x-2">
              <NuxtLink
                to="/"
                :class="[
                  isActiveLink('/')
                    ? 'bg-green-900'
                    : 'hover:bg-gray-900 hover:text-white',
                  'text-white',
                  'px-3',
                  'py-2',
                  'rounded-md',
                ]"
                >Home</NuxtLink
              >
              <NuxtLink
                to="/jobs"
                :class="[
                  isActiveLink('/jobs')
                    ? 'bg-green-900'
                    : 'hover:bg-gray-900 hover:text-white',
                  'text-white',
                  'px-3',
                  'py-2',
                  'rounded-md',
                ]"
                >Jobs</NuxtLink
              >
              <NuxtLink
                to="/jobs/add"
                :class="[
                  isActiveLink('/jobs/add')
                    ? 'bg-green-900'
                    : 'hover:bg-gray-900 hover:text-white',
                  'text-white',
                  'px-3',
                  'py-2',
                  'rounded-md',
                ]"
                >Add Job</NuxtLink
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>
