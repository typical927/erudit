<template>
  <div class="footer">
    <header class="absolute inset-x-0 bottom-0 z-50">
      <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-900" @click="mobileMenuOpen = true">
            <span class="sr-only">See More</span>
            <ChevronUpIcon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <NuxtLink v-for="item in navigation" :key="item.name" :href="item.href" class="text-lg font-semibold leading-6 text-gray-900">{{ item.name }}</NuxtLink>
        </div>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
        </div>
      </nav>
      <Dialog as="div" class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-gray-900 px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-white">
          <div class="flex items-center justify-between">
            <NuxtLink href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">See More</span>
              <img class="h-8 w-auto" src="https://pbs.twimg.com/media/EcNh2IRUcAEgURc.png" alt="miku" />
            </NuxtLink>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-white" @click="mobileMenuOpen = false">
              <span class="sr-only">Close</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <NuxtLink v-for="item in navigation" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-white hover:bg-gray-900">{{ item.name }}</NuxtLink>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>
  </div>
</template>

<script lang="ts" setup>
  import { ref } from 'vue'
  import { Dialog, DialogPanel } from '@headlessui/vue'
  import { Bars3Icon, XMarkIcon, ChevronUpIcon } from '@heroicons/vue/24/outline'

  const navigation = [
    { name: 'About Us', href: '/about-us' },
    { name: 'Contact Us', href: '/contact-us' },
  ]

  const mobileMenuOpen = ref(false)
</script>

<style>
.footer {
    bottom: 0;
    position: sticky;
    height: auto;
}
</style>
