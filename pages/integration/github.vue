<template>
  <div class="lg:grid lg:grid-cols-12 lg:gap-8">
    <div
      class="sm:text-center md:max-w-2xl md:mx-auto lg:col-span-6 lg:text-left"
    >
      <h1>
        <span
          class="mt-1 block text-4xl tracking-tight font-extrabold sm:text-5xl xl:text-6xl"
        >
          <span class="block text-gray-900">GitHub + Bytebase</span>
          <span class="block text-indigo-600">Database-as-Code</span>
        </span>
      </h1>
      <h2
        class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl"
      >
        {{ $t("integration.github-feature") }}
        <nuxt-link
          :to="localePath('/docs/vcs-integration/github-com')"
          target="_blank"
          class="text-blue-700"
          >{{ $t("integration.view-detailed-guide") }}</nuxt-link
        >
      </h2>
      <div
        class="mt-8 sm:max-w-lg sm:mx-auto sm:text-center lg:text-left lg:mx-0"
      >
        <ActionSection :module-name="'integration'" />
      </div>
    </div>
    <div
      class="mt-12 relative sm:max-w-lg sm:mx-auto lg:mt-0 lg:max-w-none lg:mx-0 lg:col-span-6 lg:flex lg:items-center"
    >
      <div class="relative mx-auto w-full rounded-lg lg:max-w-md">
        <img class="w-full" src="~/assets/bytebase_and_github.webp" alt="" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({
  layout: "integration",
  head: {
    title: "Integration with GitHub",
    meta: [
      {
        hid: "Integration with GitHub",
        name: "Integration with GitHub",
        content:
          "Bytebase integrates with GitHub to allow team to manage database migration scripts in the GitHub repository. Migration pipeline is triggered on observing new migration script push event.",
      },
    ],
  },
});
</script>
