<template>
    <div class="container mx-auto" style="min-height: 90vh">
        <div class="grid md:grid-cols-6 gap-7 md:items-center text-white h-full">
            <div class="col-span-12 md:col-span-3">
                <div class="clashdisplay-bold text-white text-2xl text-left md:text-center mt-4 px-10 md:hidden">
                    <div class="text-[#D434FE]">Register</div>
                </div>
                <img src="../assets/images/3d-graphic-designer.svg" class="w-1/2 md:w-full mx-auto floating-image" />
            </div>
            <div class="col-span-12 md:col-span-3">
                <div class="glass p-10 pt-0 md:pt-10">

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
                    <div class="clashdisplay-bold text-white text-2xl text-left md:text-center hidden md:block">
                        <div class="text-[#D434FE]">Register</div>
                    </div>
                    <div class="text-white text-sm my-4 font-normal font-['Montserrat'] text-center md:text-left">Be part of
                        this movement!</div>
                    <div class="text-white text-2xl font-normal font-['Montserrat'] mt-4 text-center md:text-left">CREATE
                        YOUR ACCOUNT</div>
                    <div class="grid md:grid-cols-2 gap-4 mt-5">
                        <!-- Name -->
                        <div>
                            <p class="text-white monserrat-reg mb-2">Team's Name</p>
                            <div class="relative mb-4 " data-te-input-wrapper-init>
                                <input type="text" v-model="form.team_name"
                                    class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                                    id="exampleFormControlInput3" placeholder="Enter the name of your group" />
                            </div>
                        </div>

                        <!-- Phone -->
                        <div>
                            <p class="text-white monserrat-reg mb-2">Phone</p>
                            <div class="relative mb-4 " data-te-input-wrapper-init>
                                <input type="number" v-model="form.phone_number"
                                    class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                                    id="exampleFormControlInput3" placeholder="Enter your phone number" />
                            </div>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-2 gap-4 mt-8">
                        <!-- Email -->
                        <div>
                            <p class="text-white monserrat-reg mb-2">Email</p>
                            <div class="relative mb-4 " data-te-input-wrapper-init>
                                <input type="email" v-model="form.email"
                                    class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                                    id="exampleFormControlInput3" placeholder="Enter your email address" />
                            </div>
                        </div>

                        <!-- project -->
                        <div>
                            <p class="text-white monserrat-reg mb-2">Project topic</p>
                            <div class="relative mb-4 " data-te-input-wrapper-init>
                                <input type="text" v-model="form.project_topic"
                                    class="peer block min-h-[auto] w-full rounded border-0 bg-transparent px-3 py-[0.32rem] leading-[2.15] outline-none transition-all duration-200 ease-linear focus:placeholder:opacity-100 data-[te-input-state-active]:placeholder:opacity-100 motion-reduce:transition-none dark:text-neutral-200 dark:placeholder:text-neutral-200 [&:not([data-te-input-placeholder-active])]:placeholder:opacity-0"
                                    id="exampleFormControlInput3" placeholder="Enter your group project topic" />
                            </div>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-2 gap-4 mt-8">
                        <div>
                            <p class="text-white monserrat-reg mb-2">Category</p>
                            <select data-te-select-init data-te-select-size="lg" v-model="form.category">
                                <option :value="item.id" v-for="item in category" :key="item.id">{{ item.name }}</option>
                            </select>
                        </div>


                        <!-- Email -->
                        <div>
                            <p class="text-white monserrat-reg mb-2">Group size</p>
                            <select data-te-select-init data-te-select-size="lg" v-model="form.group_size">
                                <option :value="item" v-for="(item, index) in groupSizeList" :key="index">{{ item }}
                                </option>
                            </select>
                        </div>
                    </div>

                    <div class="text-pink-500 text-sm font-normal monserrat-med-italic mt-8">Please review your registration
                        details before submitting</div>
                    <div class="mt-5">
                        <div class="mb-[0.125rem] block min-h-[1.5rem] pl-[1.5rem]">
                            <input v-model="form.privacy_poclicy_accepted"
                                class="relative float-left -ml-[1.5rem] mr-[6px] mt-[0.15rem] h-[1.125rem] w-[1.125rem] appearance-none rounded-[0.25rem] border-[0.125rem] border-solid border-neutral-300 outline-none before:pointer-events-none before:absolute before:h-[0.875rem] before:w-[0.875rem] before:scale-0 before:rounded-full before:bg-transparent before:opacity-0 before:shadow-[0px_0px_0px_13px_transparent] before:content-[''] checked:border-primary checked:bg-primary checked:before:opacity-[0.16] checked:after:absolute checked:after:-mt-px checked:after:ml-[0.25rem] checked:after:block checked:after:h-[0.8125rem] checked:after:w-[0.375rem] checked:after:rotate-45 checked:after:border-[0.125rem] checked:after:border-l-0 checked:after:border-t-0 checked:after:border-solid checked:after:border-white checked:after:bg-transparent checked:after:content-[''] hover:cursor-pointer hover:before:opacity-[0.04] hover:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:shadow-none focus:transition-[border-color_0.2s] focus:before:scale-100 focus:before:opacity-[0.12] focus:before:shadow-[0px_0px_0px_13px_rgba(0,0,0,0.6)] focus:before:transition-[box-shadow_0.2s,transform_0.2s] focus:after:absolute focus:after:z-[1] focus:after:block focus:after:h-[0.875rem] focus:after:w-[0.875rem] focus:after:rounded-[0.125rem] focus:after:content-[''] checked:focus:before:scale-100 checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca] checked:focus:before:transition-[box-shadow_0.2s,transform_0.2s] checked:focus:after:-mt-px checked:focus:after:ml-[0.25rem] checked:focus:after:h-[0.8125rem] checked:focus:after:w-[0.375rem] checked:focus:after:rotate-45 checked:focus:after:rounded-none checked:focus:after:border-[0.125rem] checked:focus:after:border-l-0 checked:focus:after:border-t-0 checked:focus:after:border-solid checked:focus:after:border-white checked:focus:after:bg-transparent dark:border-neutral-600 dark:checked:border-primary dark:checked:bg-primary dark:focus:before:shadow-[0px_0px_0px_13px_rgba(255,255,255,0.4)] dark:checked:focus:before:shadow-[0px_0px_0px_13px_#3b71ca]"
                                type="checkbox" value="" id="checkboxDefault" />
                            <label class="inline-block pl-[0.15rem] hover:cursor-pointer" for="checkboxDefault">
                                <div class="text-white text-sm font-normal font-['Montserrat']">I agreed with the event
                                    terms and conditions and privacy policy</div>
                            </label>
                        </div>
                    </div>

                    <div class="">
                        <button type="button" data-te-ripple-init data-te-ripple-color="light" @click="submitForm"
                            class="monserrat-reg w-full primary-btn mt-5 mr-3 inline-block font-medium leading-normal text-white transition duration-150 ease-in-out focus:outline-none focus:ring-0 active:text-primary-700 motion-reduce:transition-none">
                            <div v-if="submittingform"
                                class="inline-block h-8 w-8 animate-spin rounded-full border-4 border-solid border-current border-r-transparent align-[-0.125em] motion-reduce:animate-[spin_1.5s_linear_infinite]"
                                role="status">
                                <span
                                    class="!absolute !-m-px !h-px !w-px !overflow-hidden !whitespace-nowrap !border-0 !p-0 ![clip:rect(0,0,0,0)]">Loading...</span>
                            </div>
                            <span v-else>Register Now</span>
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
                        <img src="../assets/images/congratulation.svg"/>
                        <div class="text-center text-white text-[32px] font-semibold font-['Montserrat'] mt-5">
                            Congratulations<br />you have successfully Registered!</div>
                        <div class="text-center text-white text-sm font-semibold font-['Montserrat'] leading-8 mt-4">Yes, it
                            was easy and you did it!<br />check your mail box for next step</div>
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
import { onMounted } from "vue"
import {
    Input,
    initTE,
    Select,
    Ripple,
    Modal,
    Toast
} from "tw-elements";

onMounted(() => {
    initTE({ Input, Select, Ripple, Modal, Toast });
    getCategory()
})

const category = ref([]);
const form = ref({
    group_size: 10,
    category: 1
})
const submittingform = ref(false)
const largemodal = ref(null)

const groupSizeList = ref([
    1, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100
])
const toast = ref(false)
const toastMessage = ref("")

const getCategory = async () => {
    try {
        let response = await $fetch('https://backend.getlinked.ai/hackathon/categories-list');
        console.log(category);
        category.value = response
    } catch (err) {
        console.log(err);
    }
}

const submitForm = () => {
    console.log(form.value);
    if (form.value.privacy_poclicy_accepted) {
        submittingform.value = true;
        $fetch('https://backend.getlinked.ai/hackathon/registration', {
            method: 'POST',
            body: JSON.stringify(form.value)
        }).then(res => {
            console.log(res);
            submittingform.value = false;
            form.value = {}
            largemodal.value.click();
        }).catch(err => {
            console.log(err.response, 'err.response');
            // console.log(err);
            submittingform.value = false;
            toast.value = true;
            toastMessage.value = Object.keys(err.response._data).join(", ").replaceAll("_", " ") + " are required"
        })
    } else {
        toast.value = true
        toastMessage.value = 'Kindly accept the terms and policies before proceeding'
    }
}



</script>