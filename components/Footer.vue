<script setup>
import { computed } from 'vue';
// import { Link, router, useForm } from '@inertiajs/vue3';
import { ref } from "vue";

const currentYear = computed(() => {
    const currentDate = new Date();
    return currentDate.getFullYear();
})


const form = {
    email: null
}

const saveSubscriber = () => {
    // form.post(route('save-subscriber'), {
    //     preserveState: true,
    //     preserveScroll: true,
    //     onSuccess: (response) => {
    //         console.log(response)
    //         form.reset();
    //     },
    // })
}


</script>

<template>
    <div>

        <footer class="bg-black" aria-labelledby="footer-heading">
            <h2 id="footer-heading" class="sr-only">Footer</h2>
            <div class="mx-auto max-w-7xl px-6 pb-8 pt-16 sm:pt-10">
                <div class="xl:grid xl:grid-cols-3 xl:gap-8">
                    <div>
                        <img data-wow-delay="1s" class="wow animate__lightSpeedInLeft h-20 w-18" src="/img/logo.jpg"
                            alt="Commercial Kitchen">
                        <div class="max-w-xl lg:max-w-lg mt-5">
                            <h2 class="text-md font-medium tracking-tight text-white sm:text-xl">Subscribe to our
                                newsletter.</h2>
                            <div class="mt-2 flex max-w-md gap-x-4">
                                <label for="email-address" class="sr-only">Email address</label>
                                <input v-model="form.email" id="email-address" name="email" type="email"
                                    autocomplete="email" required
                                    class="min-w-0 flex-auto border-0 bg-white px-3.5 py-2 text-black font-bold shadow-sm ring-1 ring-inset ring-white/10 focus:ring-2 focus:ring-inset focus:ring-primary sm:text-sm text-xs sm:leading-6"
                                    placeholder="Enter your email">
                                <button @click="saveSubscriber" type="submit"
                                    class="flex-none bg-white px-3.5 py-2.5 text-sm font-semibold text-black shadow-sm hover:bg-primary focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Subscribe</button>
                            </div>
                        </div>
                        <div>
                            <!-- <p v-if="form.errors.email" class="text-white mt-5 text-xs"><i
                                    class="fa-regular fa-circle-exclamation fa-xl mr-2 text-primary font-semibold"></i>
                                {{ form.errors.email }}</p> -->
                        </div>
                    </div>
                    <div class="mt-16 grid sm:grid-cols-2 grid-cols-1 gap-8 xl:col-span-2 xl:mt-0">
                        <div class="hidden sm:flex w-full md:grid md:grid-cols-2 md:gap-8">

                        </div>
                        <div class="flex gap-32 sm:gap-0 md:grid md:grid-cols-2 grid-cols-1 md:gap-8">
                            <div>
                                <h3 class="text-sm font-semibold leading-6 text-primary">Quick Links</h3>
                                <ul role="list" class="mt-6 space-y-4">
                                    <li>
                                        <button 
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                            class="mr-2 fas fa-caret-right"></i> Services</button>
                                    </li>
                                    <li>
                                        <button
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                            class="mr-2 fas fa-caret-right"></i> Contact Us</button>
                                    </li>
                                    <li>
                                        <button
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                            class="mr-2 fas fa-caret-right"></i> About Us</button>
                                    </li>
                                </ul>
                            </div>
                            <div class="sm:mt-10 md:mt-0">
                                <h3 class="text-sm font-semibold leading-6 text-primary">Helper Links</h3>
                                <ul role="list" class="mt-6 space-y-4">
                                    <li>
                                        <button
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                            class="mr-2 fas fa-caret-right"></i> Blogs</button>
                                    </li>
                                    <li>
                                        <button
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                            class="mr-2 fas fa-caret-right"></i> Gallery</button>
                                    </li>
                                    <li>
                                        <button @click="careerModal = true"
                                            class="text-sm leading-6 text-white hover:text-primary"><i
                                                class="mr-2 fas fa-caret-right"></i> Careers</button>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-8 border-t border-white/10 pt-8 md:flex md:items-center md:justify-between">
                    <div class="flex space-x-6 md:order-2">

                        <div class="flex gap-10 mt-2">
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/fb.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/ig.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/twitter.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/linkedin.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/youtube.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                            <a href="https://www.instagram.com/commercialkitchensconsultants/" target="_blank">
                                <img src="/img/tiktok.svg" alt="" class="tranform transition hover:scale-125 duration-700 ease-in-out h-8 w-8">
                            </a>
                        </div>
                    </div>
                    <p class="mt-8 text-xs leading-5 text-white md:order-1 md:mt-0">&copy; {{ currentYear }} Commercial
                        Kitchen Equipment
                    </p>
                    <p class="mt-8 text-xs leading-5 text-white md:order-1 md:mt-0">Designed by <a
                            href="https://www.linkedin.com/in/michaelsaiba/" target="_blank"
                            class="text-primary underline">Michael Saiba</a> </p>
                </div>
            </div>
        </footer>

    </div>
</template>