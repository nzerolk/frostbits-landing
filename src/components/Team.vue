<template>
  <div class="bg-gray-900 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-400">About us</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-white sm:text-4xl">The Company</p>
        <p class="mt-6 text-lg leading-8 text-gray-300">As a Canadian enterprise, we take pride in our commitment to delivering innovative solutions. Our team of global industry experts is dedicated to bring your business solution from zero to hero.</p>
      </div>
      <ul role="list" class="mx-auto my-20 grid max-w-2xl grid-cols-2 gap-x-8 gap-y-16 text-center sm:grid-cols-2 md:grid-cols-4 lg:mx-0 lg:max-w-none">
        <li v-for="person in people" :key="person.name">
          <a :href="person.link" target="_blank">
            <img class="mx-auto h-24 w-24 rounded-full" :src="person.imageUrl" alt="" />
            <h3 class="mt-6 text-base font-semibold leading-7 tracking-tight text-white">{{ person.name }}</h3>
          </a>
          <p class="text-sm leading-6 text-indigo-400">{{ person.role }}</p>
        </li>
      </ul>
      <div class="mx-auto max-w-2xl lg:text-center">
        <p class="mt-6 text-lg leading-8 text-gray-300">Transform your passion into profit! Join our global network of industry experts and turn your free time into earning opportunities. Through our bounty-based system, we engage with top-tier consultants to build solutions that are both cost-effective and of the highest caliber.</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const people = [
  {
    name: 'Wilder Stubbs',
    role: 'CEO & Co-Founder',
    imageUrl: '/Wilder.png',
    link: 'https://x.com/WilderStubbs'
  },
  {
    name: 'Corentin Thomasset',
    role: 'Solution Architect & Co-Founder',
    imageUrl: '/Corentin.png',
    link: 'https://github.com/nzerolk'
  },
]
</script>
