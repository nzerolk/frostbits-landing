<template>
  <div class="bg-gray-900 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-400">About us</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-white sm:text-4xl">The Company</p>
        <p class="mt-6 text-lg leading-8 text-gray-300">As a Canadian enterprise, we take pride in our commitment to delivering innovative solutions. Our team of global industry experts is dedicated to bring your business solution from zero to hero.</p>
      </div>
      <ul role="list" class="mx-auto my-20 flex max-w-2xl justify-center gap-x-8 gap-y-16 text-center flex-wrap lg:mx-0 lg:max-w-none">
        <li v-for="person in people" :key="person.name" class="w-56">
          <img class="mx-auto h-24 w-24 rounded-full" :src="person.imageUrl" alt="" />
          <h3 class="mt-6 text-base font-semibold leading-7 tracking-tight text-white">{{ person.name }}</h3>
          <p class="text-sm leading-6 text-indigo-400">{{ person.role }}</p>
          <div class="mt-2 flex justify-center space-x-10" v-if="person.socials">
            <a v-for="item in person.socials" :key="item.name" :href="item.href" class="text-gray-400 hover:text-gray-500">
              <span class="sr-only">{{ item.name }}</span>
              <component :is="item.icon" class="h-6 w-6" aria-hidden="true" />
            </a>
          </div>
        </li>
      </ul>
      <div class="mx-auto max-w-2xl lg:text-center">
        <p class="mt-6 text-lg leading-8 text-gray-300">Transform your passion into profit ! Join our global network of industry experts and turn your free time into earning opportunities. Through our bounty-based system we engage with top-tier consultants to build solutions that are both cost-effective and of the highest caliber. </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import {defineComponent, h} from "vue";

const people = [
  {
    name: 'Wilder Stubbs',
    role: 'CEO & Co-Founder',
    imageUrl: '/Wilder.png',
    socials: [{
      name: 'X',
      href: 'https://x.com/WilderStubbs',
      icon: defineComponent({
        render: () =>
            h('svg', { fill: 'currentColor', viewBox: '0 0 24 24' }, [
              h('path', {
                d: 'M13.6823 10.6218L20.2391 3H18.6854L12.9921 9.61788L8.44486 3H3.2002L10.0765 13.0074L3.2002 21H4.75404L10.7663 14.0113L15.5685 21H20.8131L13.6819 10.6218H13.6823ZM11.5541 13.0956L10.8574 12.0991L5.31391 4.16971H7.70053L12.1742 10.5689L12.8709 11.5655L18.6861 19.8835H16.2995L11.5541 13.096V13.0956Z',
              }),
            ]),
      }),
    }]
  },
  {
    name: 'Corentin Thomasset',
    role: 'Co-Founder & Solution Architect',
    imageUrl: '/Corentin.png',
  }

]
</script>