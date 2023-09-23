<template>
    <div class="container mx-auto" style="min-height: 90vh">
        <div class="grid md:grid-cols-6 gap-7 md:items-center text-white h-full">
            <div class="hidden md:block md:col-span-3">
                <div class="text-center md:text-left">
                    <div class="clashdisplay-bold text-white text-3xl text-center md:text-left">
                        <span class="text-[#D434FE] ">Get in touch</span>
                    </div>
                    <div class="text-white monserrat-reg mt-8">
                        Contact <br />Information
                    </div>
                    <div class="text-white monserrat-reg mt-8">
                        27,Alara Street<br />
                        Yaba 100012<br />
                        Lagos State
                    </div>
                    <div class="text-white monserrat-reg mt-8">
                        Call Us : 07067981819
                    </div>
                    <div class="text-white monserrat-reg mt-8">
                        we are open from Monday-Friday<br />
                        08:00am - 05:00pm
                    </div>
                    <div class="text-fuchsia-500 text-base font-normal font-['Montserrat'] mt-10 mb-4">Share on</div>
                    <img src="../assets/images/mdi_instagram.svg" class="inline" />
                    <img src="../assets/images/twitter.svg" class="inline ml-4" />
                    <img src="../assets/images/facebook.svg" class="inline ml-4" />
                    <img src="../assets/images/ri_linkedin-fill.svg" class="inline ml-4" />
                </div>
            </div>
            <div class="col-span-12 md:col-span-3 xl:col-span-2">
                <div class="glass p-10">
                    <NuxtLink to="/">
                        <img src="../assets/images/back.svg" class="mb-5 md:hidden" />
                    </NuxtLink>

                    <!-- Toast -->
                    <div v-if="toast"
                        class="pointer-events-auto mx-auto mb-4 hidden w-96 max-w-full rounded-lg bg-danger-100 bg-clip-padding text-sm text-danger-700 shadow-lg shadow-black/5 data-[te-toast-show]:block data-[te-toast-hide]:hidden"
                        id="static-example" role="alert" aria-live="assertive" aria-atomic="true" data-te-autohide="false"
                        data-te-toast-init data-te-toast-show>
                        <div
                            class="flex items-center justify-between rounded-t-lg border-b-2 border-danger-200 bg-danger-100 bg-clip-padding px-4 pb-2 pt-2.5 text-danger-700">
                            <p class="flex items-center font-bold text-danger-700">
                                <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="times-circle"
                                    class="mr-2 h-4 w-4 fill-current" role="img" xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 512 512">
                                    <path fill="currentColor"
                                        d="M256 8C119 8 8 119 8 256s111 248 248 248 248-111 248-248S393 8 256 8zm121.6 313.1c4.7 4.7 4.7 12.3 0 17L338 377.6c-4.7 4.7-12.3 4.7-17 0L256 312l-65.1 65.6c-4.7 4.7-12.3 4.7-17 0L134.4 338c-4.7-4.7-4.7-12.3 0-17l65.6-65-65.6-65.1c-4.7-4.7-4.7-12.3 0-17l39.6-39.6c4.7-4.7 12.3-4.7 17 0l65 65.7 65.1-65.6c4.7-4.7 12.3-4.7 17 0l39.6 39.6c4.7 4.7 4.7 12.3 0 17L312 256l65.6 65.1z">
                                    </path>
                                </svg>
                                Oops😔
                            </p>
                            <div class="flex items-center">
                                <button type="button"
                                    class="ml-2 box-content rounded-none border-none opacity-80 hover:no-underline hover:opacity-75 focus:opacity-100 focus:shadow-none focus:outline-none"
                                    data-te-toast-dismiss aria-label="Close">
                                    <span @click="toast = false"
                                        class="w-[1em] focus:opacity-100 disabled:pointer-events-none disabled:select-none disabled:opacity-25 [&.disabled]:pointer-events-none [&.disabled]:select-none [&.disabled]:opacity-25">
                                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                            stroke-width="1.5" stroke="currentColor" class="h-6 w-6">
                                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                                        </svg>
                                    </span>
                                </button>
                            </div>
                        </div>
                        <div class="break-words rounded-b-lg bg-danger-100 px-4 py-4 text-danger-700">
                            {{ toastMessage }}
                        </div>
                    </div>

                    <div class="clashdisplay-bold text-white text-2xl text-left md:text-center">
                        <div class="text-[#D434FE] ">Questions or need assistance?</div>
                        <div class="text-[#D434FE] mt-4">Let us know about it!</div>
                    </div>
                    <div class="text-white text-sm my-8 md:hidden font-normal font-['Montserrat']">Email us below to any
                        question related <br />to our event</div>
                    <div class="relative mb-3 mt-8" data-te-input-wrapper-init>
                        <input type="text"
                            class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                            id="exampleFormControlInput2" placeholder="First Name" v-model="form.first_name" />
                        <label for="exampleFormControlInput2"
                            class="pointer-events-none absolute left-3 top-0 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[2.15] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[1.15rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[1.15rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary">
                            First Name
                        </label>
                    </div>
                    <div class="relative mb-3 mt-8" data-te-input-wrapper-init>
                        <input type="email"
                            class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                            id="exampleFormControlInput1" placeholder="Mail" v-model="form.email" />
                        <label for="exampleFormControlInput1"
                            class="pointer-events-none absolute left-3 top-0 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[2.15] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[1.15rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[1.15rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary">
                            Email
                        </label>
                    </div>
                    <div class="relative mb-3 mt-8" data-te-input-wrapper-init>
                        <input type="number"
                            class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                            id="exampleFormControlInput1" placeholder="Phone number" v-model="form.phone_number" />
                        <label for="exampleFormControlInput1"
                            class="pointer-events-none absolute left-3 top-0 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[2.15] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[1.15rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[1.15rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary">
                            Phone number
                        </label>
                    </div>
                    <div class="relative mb-3 mt-8" data-te-input-wrapper-init>
                        <textarea
                            class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[1.6] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 peer-focus:text-primary data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 dark:peer-focus:text-primary [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                            id="exampleFormControlTextarea1" rows="4" placeholder="Your message"
                            v-model="form.message"></textarea>
                        <label for="exampleFormControlTextarea1"
                            class="pointer-events-none absolute left-3 top-0 mb-0 max-w-[90%] origin-[0_0] truncate pt-[0.37rem] leading-[1.6] text-neutral-500 transition-all duration-200 ease-out peer-focus:-translate-y-[0.9rem] peer-focus:scale-[0.8] peer-focus:text-primary peer-data-[te-input-state-active]:-translate-y-[0.9rem] peer-data-[te-input-state-active]:scale-[0.8] motion-reduce:transition-none dark:text-neutral-200 dark:peer-focus:text-primary">
                            Enter your message
                        </label>
                    </div>
                    <div class="flex justify-center">
                        <button type="button" data-te-ripple-init data-te-ripple-color="light" @click="contactus"
                            class="monserrat-reg primary-btn mt-4 mr-3 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                            <div v-if="submittingform"
                                class="inline-block h-8 w-8 animate-spin rounded-full border-4 border-solid border-current border-r-transparent align-[-0.125em] motion-reduce:animate-[spin_1.5s_linear_infinite]"
                                role="status">
                                <span
                                    class="!absolute !-m-px !h-px !w-px !overflow-hidden !whitespace-nowrap !border-0 !p-0 ![clip:rect(0,0,0,0)]">Loading...</span>
                            </div>
                            <span v-else>Submit</span>
                        </button>

                    </div>
                    <div class="flex flex-col items-center">
                        <div class="text-fuchsia-500 text-base font-normal font-['Montserrat'] mt-[50px] mb-4">Share on
                        </div>
                        <div>
                            <img src="../assets/images/mdi_instagram.svg" class="inline" />
                            <img src="../assets/images/twitter.svg" class="inline ml-4" />
                            <img src="../assets/images/facebook.svg" class="inline ml-4" />
                            <img src="../assets/images/ri_linkedin-fill.svg" class="inline ml-4" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!--Button trigger large modal-->
    <button type="button" ref="largemodal"
        class="hidden inline-block rounded bg-primary px-6 pb-2 pt-2.5 text-xs font-medium uppercase leading-normal text-white shadow-[0_4px_9px_-4px_#3b71ca] transition duration-150 ease-in-out hover:bg-primary-600 hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:bg-primary-600 focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:outline-none focus:ring-0 active:bg-primary-700 active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] dark:shadow-[0_4px_9px_-4px_rgba(59,113,202,0.5)] dark:hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)]"
        data-te-toggle="modal" data-te-target="#exampleModalLg" data-te-ripple-init data-te-ripple-color="light">
        Large modal
    </button>




    <!--Large modal-->
    <div data-te-modal-init
        class="fixed left-0 top-0 z-[1055] hidden h-full w-full overflow-y-auto overflow-x-hidden outline-none bg-[#150e28b0]"
        id="exampleModalLg" tabindex="-1" aria-labelledby="exampleModalLgLabel" aria-modal="true" role="dialog">
        <div data-te-modal-dialog-ref
            class="pointer-events-none relative w-auto translate-y-[-50px] opacity-0 transition-all duration-300 ease-in-out min-[576px]:mx-auto min-[576px]:mt-7 min-[576px]:max-w-[500px] min-[992px]:max-w-[800px] pointer-events-none relative flex min-h-[calc(100%-1rem)] w-auto translate-y-[-50px] items-center opacity-0 transition-all duration-300 ease-in-out min-[576px]:mx-auto min-[576px]:mt-7 min-[576px]:min-h-[calc(100%-3.5rem)] min-[576px]:max-w-[500px]">
            <div
                class="success-modal pointer-events-auto relative flex w-full flex-col rounded-md border-none bg-white bg-clip-padding text-current shadow-lg outline-none dark:bg-neutral-600">


                <!--Modal body-->
                <div class="relative p-10">
                    <img src="../assets/images/purplestar.svg" class="w-[20px] success-modal-star" />
                    <div class="flex flex-col items-center">
                        <img src="../assets/images/congratulation.svg" />
                        <div class="text-center text-white text-[32px] font-semibold font-['Montserrat'] mt-5">
                            Success</div>
                        <div class="text-center text-white text-sm font-semibold font-['Montserrat'] leading-8 mt-2">
                            Thanks for contacting us <br />We have received your message<br />and we'll get back to you
                            shortly</div>
                        <button type="button" data-te-ripple-init data-te-ripple-color="light" data-te-modal-dismiss
                            class="monserrat-reg w-full primary-btn mt-5 mr-3 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                            Back
                        </button>
                    </div>>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { onMounted, ref } from "vue"
import {
    Input,
    initTE,
    Ripple,
    Modal
} from "tw-elements";

onMounted(() => {
    initTE({ Input, Ripple, Modal });
})

const form = ref({})
const submittingform = ref(false)
const largemodal = ref(null)
const toast = ref(false)
const toastMessage = ref("")

const contactus = async () => {
    submittingform.value = true
    try {
        let response = await $fetch('https://backend.getlinked.ai/hackathon/contact-form', {
            method: "POST",
            body: form.value,
            headers: {
                'Content-Type': 'application/json'
            },
        })
        console.log(response);
        submittingform.value = false
        largemodal.value.click();
        form.value = {}
    } catch (err) {
        console.log(err);
        submittingform.value = false
        toast.value = true
        toastMessage.value = Object.keys(err.response._data).join(", ").replaceAll("_", " ") + ' are required'
    }
}



</script>