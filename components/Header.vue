<template>
    <!-- Main navigation container -->
    <nav class="bg-[#150e28] relative z-10 flex w-full flex-wrap items-center justify-between py-7 text-neutral-500 shadow-lg hover:text-neutral-700 focus:text-neutral-700 dark:bg-neutral-600 border-b border-b-[rgba(255,255,255,0.18)] px-5 lg:px-10"
        data-te-navbar-ref>
        <div class="flex w-full flex-wrap items-center justify-between px-3">
            <div>
                <a class="mx-2 my-1 flex items-center text-neutral-900 hover:text-neutral-900 focus:text-neutral-900 lg:mb-0 lg:mt-0"
                    href="#">
                    <NuxtLink to="/">
                        <Transition>
                            <img v-show="!displayNav" class="mr-2 mr-2 w-1/2 lg:w-full" src="../assets/images/getlinked.svg" alt="getlinked"
                                loading="lazy" />
                        </Transition>
                    </NuxtLink>
                </a>
            </div>

            <!-- Hamburger button for mobile view -->
            <button @click="toggleNav"
                class="block border-0 bg-transparent px-2 text-neutral-500 hover:no-underline hover:shadow-none focus:no-underline focus:shadow-none focus:outline-none focus:ring-0 dark:text-neutral-200 lg:hidden"
                type="button" data-te-collapse-init data-te-target="#navbarSupportedContent4"
                aria-controls="navbarSupportedContent4" aria-expanded="false" aria-label="Toggle navigation">
                <!-- Hamburger icon -->
                <span>

                    <div class="close-nav flex justify-center items-center" v-show="displayNav">
                        <div class="flex justify-center items-center h-[20px] w-[20px] rounded-full bg-[#150e28]">
                            <img src="../assets/images/close-nav.png" ref="closeref" />
                        </div>
                    </div>
                    <img src="../assets/images/hambuger.svg" class="w-[20px]" v-show="!displayNav" />
                    <!-- <img src="../assets/images/close-nav.png" v-else class="w-[25px]" /> -->
                </span>
            </button>

            <!-- Collapsible navbar container -->
            <div class="!visible mt-2 hidden flex-grow basis-[100%] items-center lg:mt-0 lg:!flex lg:basis-auto"
                id="navbarSupportedContent4" data-te-collapse-item>
                <div class="!visible mt-2 hidden flex-grow basis-[100%] items-center lg:mt-0 lg:!flex lg:basis-auto"
                    id="navbarSupportedContent2" data-te-collapse-item>

                </div>
                <div class="lg:flex lg:items-center">
                    <!-- Left links -->
                    <ul class="list-style-none ml-auto flex flex-col pl-0 lg:mt-1 lg:flex-row" data-te-navbar-nav-ref>

                        <!-- Pricing link -->
                        <li class="mb-4 pl-2 lg:mb-0 lg:pl-0 lg:pr-1 mr-10" data-te-nav-item-ref>
                            <a class="monserrat-semibold p-0 text-white transition duration-200 hover:ease-in-out focus:bg-gradient-to-r focus:from-purple-500 focus:to-pink-500 focus:bg-clip-text focus:text-transparent focus:transition focus:duration-300 hover:bg-gradient-to-r hover:from-purple-500 hover:to-pink-500 hover:bg-clip-text hover:text-transparent hover:transition hover:duration-300 disabled:text-black/30 motion-reduce:transition-none dark:text-neutral-200 dark:hover:text-neutral-400 dark:focus:text-neutral-400 lg:px-2 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                                href="#" data-te-nav-link-ref>Timeline</a>
                        </li>
                        <!-- Pricing link -->
                        <li class="mb-4 pl-2 lg:mb-0 lg:pl-0 lg:pr-1 mr-10" data-te-nav-item-ref>
                            <a class="monserrat-semibold p-0 text-white transition duration-200 hover:ease-in-out focus:bg-gradient-to-r focus:from-purple-500 focus:to-pink-500 focus:bg-clip-text focus:text-transparent focus:transition focus:duration-300 hover:bg-gradient-to-r hover:from-purple-500 hover:to-pink-500 hover:bg-clip-text hover:text-transparent hover:transition hover:duration-300 disabled:text-black/30 motion-reduce:transition-none dark:text-neutral-200 dark:hover:text-neutral-400 dark:focus:text-neutral-400 lg:px-2 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                                href="#" data-te-nav-link-ref>Overview</a>
                        </li>
                        <!-- Pricing link -->
                        <li class="mb-4 pl-2 lg:mb-0 lg:pl-0 lg:pr-1 mr-10" data-te-nav-item-ref>
                            <a class="monserrat-semibold p-0 text-white transition duration-200 hover:ease-in-out focus:bg-gradient-to-r focus:from-purple-500 focus:to-pink-500 focus:bg-clip-text focus:text-transparent focus:transition focus:duration-300 hover:bg-gradient-to-r hover:from-purple-500 hover:to-pink-500 hover:bg-clip-text hover:text-transparent hover:transition hover:duration-300 disabled:text-black/30 motion-reduce:transition-none dark:text-neutral-200 dark:hover:text-neutral-400 dark:focus:text-neutral-400 lg:px-2 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                                href="#" data-te-nav-link-ref>FAQs</a>
                        </li>
                        <!-- Pricing link -->
                        <li class="mb-4 pl-2 lg:mb-0 lg:pl-0 lg:pr-1 mr-12" data-te-nav-item-ref>
                            <!-- <NuxtLink to="/contactus"> -->
                                <a @click="reloadpage(2)" class=" monserrat-semibold p-0 text-white transition duration-200 hover:ease-in-out focus:bg-gradient-to-r focus:from-purple-500 focus:to-pink-500 focus:bg-clip-text focus:text-transparent focus:transition focus:duration-300 hover:bg-gradient-to-r hover:from-purple-500 hover:to-pink-500 hover:bg-clip-text hover:text-transparent hover:transition hover:duration-300 disabled:text-black/30 motion-reduce:transition-none dark:text-neutral-200 dark:hover:text-neutral-400 dark:focus:text-neutral-400 lg:px-2 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                                    href="#" data-te-nav-link-ref>Contacts</a>
                            <!-- </NuxtLink> -->
                        </li>

                    </ul>
                    <!-- <NuxtLink to="/register"> -->
                        <button @click="reloadpage(1)" type="button" data-te-ripple-init data-te-ripple-color="light"
                            class="monserrat-reg primary-btn mr-3 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                            Register
                        </button>
                    <!-- </NuxtLink> -->

                </div>
            </div>
        </div>
    </nav>
</template>

<script setup>
import { onMounted, ref } from "vue";
// Initialization for ES Users
import {
    Collapse,
    initTE,
} from "tw-elements";

onMounted(() => {
    initTE({ Collapse });
})

const displayNav = ref(false)
const closeref = ref(null)

const reloadpage = (type) => {
    // window.location.reload(true)
    if (type == 1) {
        window.location.href = `${window.location.origin}/register`
    } else {
        window.location.href = `${window.location.origin}/contactus`
    }
}

const toggleNav = () => {
    displayNav.value = !displayNav.value

    if (displayNav.value) {
        setTimeout(() => {
            closeref.value.classList.add('roll-in')
            closeref.value.classList.remove('roll-out')
        }, 50);
    } else {
        setTimeout(() => {
            closeref.value.classList.remove('roll-in')
            closeref.value.classList.add('roll-out')
        }, 50);
    }
}
</script>