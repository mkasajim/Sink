<script setup>
// Removed unused icon imports
const { title } = useAppConfig() // Removed unused variables
</script>

<template>
  <section class="md:pt-6">
    <div class="container flex flex-col items-center py-8 mx-auto sm:flex-row">
      <a
        href="https://라테라.xyz"
        class="text-xl font-black leading-none text-gray-900 select-none dark:text-gray-100 logo"
        :title="title"
      >{{ title }}</a>
      <span class="mt-4 text-sm text-gray-500 sm:ml-4 sm:pl-4 sm:border-l sm:border-gray-200 sm:mt-0">
        &copy; {{ new Date().getFullYear() }}
      </span>
    </div>
  </section>
</template>
