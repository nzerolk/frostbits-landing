<template>
  <div class="bg-gray-900 py-24 sm:py-32" id="work-with-us">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-base font-semibold leading-7 text-indigo-400">Build engagement</h2>
        <p class="mt-2 text-3xl font-bold tracking-tight text-white sm:text-4xl">Work with us</p>
        <p class="mt-6 text-lg leading-8 text-gray-300">Our skilled professionals are eager to solve your complex user engagement challenges. We specialize in custom cutting edge software that leverage decentralized networks to facilitate rapid, secure, and cost-effective exchange of digital goods, providing clients access to new digital ecosystems and gain a competitive advantage by keeping their community engaged.</p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
        <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-16 lg:max-w-none lg:grid-cols-3">
          <div v-for="feature in features" :key="feature.name" class="flex flex-col">
            <dt class="flex items-center gap-x-3 text-base font-semibold leading-7 text-white">
              <component :is="feature.icon" class="h-5 w-5 flex-none text-indigo-400" aria-hidden="true" />
              {{ feature.name }}
            </dt>
            <dd class="mt-4 flex flex-auto flex-col text-base leading-7 text-gray-300">
              <p class="flex-auto">{{ feature.description }}</p>
              <p class="mt-6" v-if="feature.href">
                <a :href="feature.href" class="text-sm font-semibold leading-6 text-indigo-400">Learn more <span aria-hidden="true">→</span></a>
              </p>
            </dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
import { GiftIcon, UserGroupIcon, CurrencyDollarIcon } from '@heroicons/vue/20/solid'

const features = [
  {
    name: 'Fidelity rewards',
    description:
        'Reward your most your most loyal customers with a custom loyalty program that incentivizes them to keep coming back.',
    icon: GiftIcon,
  },
  {
    name: 'Membership management',
    description:
        'Manage your community with ease. Leverage a custom platform to create and manage your own membership program.',
    icon: UserGroupIcon,
  },
  {
    name: 'Monetization platforms',
    description:
        'Monetize your content with a custom platform that allows you to sell digital goods and services to your community.',
    icon: CurrencyDollarIcon,
  },
]
</script>