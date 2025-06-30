<script setup>
import { useAppConfig } from '#imports'
import { AreaChart } from 'lucide-vue-next'

const { title } = useAppConfig()

definePageMeta({
  layout: 'landing',
})
</script>

<template>
  <main class="flex flex-col justify-center items-center min-h-[80vh]">
    <div class="text-center max-w-2xl mx-auto p-8">
      <h1 class="text-5xl font-bold mb-6">
        {{ title }}
      </h1>
      <h2 class="text-3xl font-semibold mb-8">
        {{ $t('home.cta.title') }}
      </h2>
      <div class="flex justify-center">
        <HomeLink
          href="/dashboard"
          target="_self"
          title="Dashboard"
          class="flex items-center justify-center gap-2 text-lg px-8 py-4"
        >
          <AreaChart class="w-6 h-6" />
          {{ $t('dashboard.title') }}
        </HomeLink>
      </div>
    </div>
  </main>
</template>
