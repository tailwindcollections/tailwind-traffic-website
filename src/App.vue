<script setup>
import PlayIcon from "./icons/play.svg";
import GoogleLogo from "./icons/google-logo.svg";
import FacebookLogo from "./icons/facebook-logo.svg";
import LogitechLogo from "./icons/logitech-logo.svg";
import TokopediaLogo from "./icons/tokopedia-logo.svg";
import PullAndBearLogo from "./icons/pull-and-bear-logo.svg";
import SpeakerPhoneIcon from "./icons/speakerphone.svg";
import ShoppingBagIcon from "./icons/shopping-bag.svg";
import ChipIcon from "./icons/chip.svg";
import ChartIcon from "./icons/chart.svg";

const menu = ["Rankings", "Data", "Solution", "Pricing", "Resources"];
const features = [
  {
    icon: SpeakerPhoneIcon,
    title: "Digital Marketing",
  },
  {
    icon: ShoppingBagIcon,
    title: "E-Commerce",
  },
  {
    icon: ChipIcon,
    title: "Digital Research",
  },
  {
    icon: ChartIcon,
    title: "Digital Analysis",
  },
];
</script>

<template>
  <div class="overflow-hidden w-full min-h-screen font-sans bg-gray-900">
    <div class="relative">
      <img class="absolute opacity-70" src="/img/bg-1.svg" alt="" />
      <div class="relative py-10 px-8 mx-auto max-w-7xl">
        <nav class="flex justify-between items-center">
          <a href="#" class="text-2xl font-semibold text-white">Liondo</a>
          <ul class="flex gap-x-16 items-center tracking-wider text-gray-300">
            <li v-for="item in menu" class="transition hover:text-white">
              <a href="#"> {{ item }} </a>
            </li>
          </ul>
          <button
            class="py-3 px-6 font-medium tracking-wider leading-5 text-white rounded-md border-2 border-gray-800 transition hover:text-gray-900 hover:bg-teal-300"
          >
            Get Started
          </button>
        </nav>
      </div>
      <div class="relative py-10 px-8 mx-auto max-w-7xl">
        <div class="flex">
          <div class="w-1/2">
            <h1 class="pt-10 text-7xl font-bold leading-tight text-white">
              Tracking User
              <span
                class="relative z-10 after:w-80 after:h-5 after:bg-gradient-to-l after:from-teal-300 after:absolute after:left-0 after:bottom-2 after:-z-10"
              >
                Movements
              </span>
              Around the World
            </h1>
            <p class="pt-2 max-w-lg text-xl tracking-wide leading-relaxed text-gray-300">
              Whether it's your family or your business, we want to help you take care of
              the things that matter the most.
            </p>
            <div class="flex gap-x-6 items-center pt-12">
              <button
                class="py-4 px-6 font-medium tracking-wide bg-teal-200 rounded-lg shadow-md transition hover:bg-teal-300"
              >
                Get Trial Project
              </button>
              <button
                class="flex gap-x-2 items-center py-4 px-6 font-medium tracking-wide text-gray-300 transition hover:text-teal-300"
              >
                <PlayIcon class="w-8 h-8 stroke-current" />
                <span>Watch Demo</span>
              </button>
            </div>
          </div>
          <div class="flex justify-center items-center pl-24 w-1/2">
            <img src="/img/hero.png" alt="" class="max-w-xl drop-shadow-2xl" />
          </div>
        </div>
      </div>
    </div>
    <div class="relative">
      <img class="absolute opacity-70" src="/img/bg-2.svg" alt="" />
      <div class="relative py-16 px-8 mx-auto max-w-7xl">
        <div class="flex justify-between items-center">
          <span class="font-semibold tracking-wider text-white uppercase">
            Trusted by global brands
          </span>
          <div class="flex gap-x-14 items-center">
            <GoogleLogo
              class="w-auto h-16 text-gray-400 transition cursor-pointer fill-current hover:text-white"
            />
            <FacebookLogo
              class="w-auto h-20 text-gray-400 transition cursor-pointer fill-current hover:text-white"
            />
            <LogitechLogo
              class="w-auto h-16 text-gray-400 transition cursor-pointer fill-current hover:text-white"
            />
            <TokopediaLogo
              class="w-auto h-20 text-gray-400 transition cursor-pointer fill-current hover:text-white"
            />
            <PullAndBearLogo
              class="w-auto h-20 text-gray-400 transition cursor-pointer fill-current hover:text-white"
            />
          </div>
        </div>
      </div>
      <div class="relative py-16 px-8 mx-auto max-w-7xl">
        <div class="flex gap-x-8 justify-between">
          <div class="w-1/2">
            <h2 class="text-5xl font-bold leading-tight text-white">
              Must-Have to Win Your Online Market
            </h2>
          </div>
          <div class="w-1/2">
            <p class="pt-6 text-xl leading-relaxed text-left text-gray-300">
              Found something that works for you? Request a quote from our site or call an
              agent and we'll get back to you as soon as possible.
            </p>
            <button
              class="py-4 px-8 mt-8 font-medium tracking-wider bg-teal-200 rounded-lg transition hover:bg-teal-300"
            >
              Get Started
            </button>
          </div>
        </div>
        <div class="flex gap-x-8 items-start py-16">
          <div
            v-for="feature in features"
            class="flex overflow-hidden relative flex-col items-start p-6 w-1/4 bg-gray-800 rounded-lg transition duration-300 cursor-pointer group hover:bg-white"
          >
            <span
              class="absolute top-0 right-0 w-24 h-24 bg-teal-200 transition-transform ease-out rotate-45 translate-x-20 -translate-y-20 group-hover:translate-x-14 group-hover:-translate-y-14"
            />
            <div
              class="p-2 bg-gray-900 rounded-md transition duration-300 group-hover:bg-teal-200"
            >
              <Component
                :is="feature.icon"
                class="w-6 h-6 text-white transition duration-300 group-hover:text-gray-800"
              />
            </div>
            <span
              class="inline-block pt-6 text-2xl font-medium tracking-wide text-white transition duration-300 group-hover:text-gray-800"
            >
              {{ feature.title }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
