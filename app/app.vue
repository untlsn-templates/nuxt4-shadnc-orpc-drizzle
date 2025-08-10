<script setup lang="ts">
const colorMode = useColorMode();
</script>

<template>
  <main class="min-h-screen flex flex-col">
    <div class="text-right p-4">
      <UiButton
        size="icon"
        variant="ghost"
        class="text-2xl"
        @click="colorMode.preference = colorMode.preference == 'dark' ? 'light' : 'dark'"
      >
        <NuxtIcon
          v-if="colorMode.preference == 'dark'"
          name="lucide:moon"
        />
        <NuxtIcon
          v-else
          name="lucide:sun"
        />
      </UiButton>
    </div>
    <div class="grid place-items-center flex-1 text-4xl">
      <p>Hello World!</p>
    </div>
  </main>
</template>
