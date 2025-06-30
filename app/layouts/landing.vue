<template>
  <main class="flex flex-col min-h-screen">
    <section class="container relative z-50 h-24 select-none mx-auto">
      <div class="relative flex flex-wrap items-center justify-between h-24 px-0 mx-auto overflow-hidden font-medium border-b border-gray-200 md:overflow-visible lg:justify-center">
        <div class="flex items-center justify-start w-1/4 h-full pr-4">
          <a href="/" :title="useAppConfig().title" class="flex items-center py-4 space-x-2 text-xl font-black text-gray-900 dark:text-gray-100 md:py-0">
            <span class="flex items-center justify-center w-8 h-8 rounded-full">
              <img src="/sink.png" :alt="useAppConfig().title" class="w-full h-full rounded-full">
            </span>
            <span class="mx-2">{{ useAppConfig().title }}</span>
          </a>
        </div>
        <div class="flex flex-row items-center justify-end w-3/4 h-full space-x-2">
          <SwitchLanguage />
          <SwitchTheme />
        </div>
      </div>
    </section>

    <section class="flex flex-1">
      <div class="container mx-auto">
        <slot />
      </div>
    </section>

    <section class="md:pt-6">
      <div class="container flex flex-col items-center py-8 mx-auto sm:flex-row">
        <a href="/" class="text-xl font-black leading-none text-gray-900 select-none dark:text-gray-100 logo" :title="useAppConfig().title">{{ useAppConfig().title }}</a>
        <span class="mt-4 text-sm text-gray-500 sm:ml-4 sm:pl-4 sm:border-l sm:border-gray-200 sm:mt-0">
          &copy; {{ new Date().getFullYear() }}
        </span>
      </div>
    </section>
  </main>
</template>
