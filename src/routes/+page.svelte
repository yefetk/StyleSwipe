<script>
	import { goto } from "$app/navigation";
	import { supabase } from "$lib/supabaseClient.js";
	import { onMount } from "svelte";
	import "../app.css";
</script>

<nav class="navbar sticky top-0 navbar-dark bg-primary" id="navbar">
    <div class="container">
        <ul class="list-inside">
            <li class="mt-1 font-serif text-5xl font-normal tracking-wide text-primary-200">StyleSwipe</li>
        </ul>
        <button class="navbar-btn" data-toggle="collapse" data-target="#navbar-row" aria-expanded="false" aria-label="Toggle navigation">
            <span class="sr-only">Open navbar menu</span>
            <span class="block h-1 rounded-full bg-white"></span>
            <span class="block h-1 mt-1 rounded-full bg-white"></span>
            <span class="block h-1 mt-1 rounded-full bg-white"></span>
        </button>
        <div class="navbar-row" id="navbar-row">
            <ul class="navbar-col"></ul>
            <ul class="navbar-col"></ul>
            <ul class="navbar-col">
                <li>
                    <a class="nav-link" href="#">Home</a>
                </li>
                <li>
                    <a class="nav-link" href="#">About us</a>
                </li>
                <li>
                    <a class="nav-link" href="#">Founders</a>
                </li>
                <li>
                    <a class="nav-link" href="#">Contact us</a>
                </li>
                <li>
                    <a class="btn btn-outline btn-lg font-medium text-primary-200 capitalize border-2 border-white/20 hover:text-primary hover:bg-tertiary hover:border-tertiary" href="/signup">Get Started</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
<section class="py-16 bg-primary lg:py-32">
    <div class="container">
        <div class="row gap-y-12">
            <div class="col lg:w-6/12 text-white">
                <h1 class="mb-8 text-white">Find your dream outfits just by swiping</h1>
                <p class="mb-8">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
                <a class="btn btn-lg btn-tertiary w-full sm:w-max" href="#">Try it out!</a>
            </div>
            <div class="col lg:w-6/12">
                <img src="https://d1pnnwteuly8z3.cloudfront.net/images/a4f01840-cd76-49a6-9d2c-aded32ed05e1/345140b2-5209-425c-ad16-9502ed399f93.png" />
            </div>
        </div>
    </div>
</section>
<section class="py-16 bg-primary-50 lg:py-32">
    <div class="container">
        <div class="row gap-y-16">
            <div class="col md:w-4/12">
                <h2 class="h2 mb-4">How we work</h2>
                <p class="mb-8 text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</p>
                <a class="btn group p-0 font-medium text-secondary" href="#"></a>
            </div>
            <div class="col md:w-4/12">
                <div class="mb-12">
                    <div class="w-14 h-14 bg-secondary rounded-lg rounded-bl-xl relative mb-4">
                        <div class="w-8 h-8 bg-tertiary rounded-bl-lg absolute left-0 bottom-0"></div>
                        <div class="w-10 h-10 bg-[#5239fa] absolute top-0 right-0 rounded-bl-lg rounded-tr-lg flex justify-center items-center text-white">
                            <div>01</div>
                        </div>
                    </div>
                    <h3 class="h3 mb-4">Measurments</h3>
                    <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</p>
                </div>
                <div class="">
                    <div class="w-14 h-14 bg-secondary rounded-lg rounded-bl-xl relative mb-4">
                        <div class="w-8 h-8 bg-tertiary rounded-bl-lg absolute left-0 bottom-0"></div>
                        <div class="w-10 h-10 bg-[#5239fa] absolute top-0 right-0 rounded-bl-lg rounded-tr-lg flex justify-center items-center text-white">
                            <div>03</div>
                        </div>
                    </div>
                    <h3 class="h3 mb-4">Algorithm</h3>
                    <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</p>
                </div>
            </div>
            <div class="col md:w-4/12">
                <div class="mb-12">
                    <div class="w-14 h-14 bg-secondary rounded-lg rounded-bl-xl relative mb-4">
                        <div class="w-8 h-8 bg-tertiary rounded-bl-lg absolute left-0 bottom-0"></div>
                        <div class="w-10 h-10 bg-[#5239fa] absolute top-0 right-0 rounded-bl-lg rounded-tr-lg flex justify-center items-center text-white">
                            <div>02</div>
                        </div>
                    </div>
                    <h3 class="h3 mb-4">Sets</h3>
                    <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</p>
                </div>
                <div class="">
                    <div class="w-14 h-14 bg-secondary rounded-lg rounded-bl-xl relative mb-4">
                        <div class="w-8 h-8 bg-tertiary rounded-bl-lg absolute left-0 bottom-0"></div>
                        <div class="w-10 h-10 bg-[#5239fa] absolute top-0 right-0 rounded-bl-lg rounded-tr-lg flex justify-center items-center text-white">
                            <div>04</div>
                        </div>
                    </div>
                    <h3 class="h3 mb-4">Discounts</h3>
                    <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.</p>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="py-16">
    <div class="container">
        <div class="row">
            <div class="col relative">
                <h2 class="h2 mb-6 lg:mb-12">Some examples</h2>
                <div class="grid grid-cols-3 gap-x-8 gap-y-8">
                    <div class="col-span-3 lg:col-span-2">
                        <div class="block relative group h-full overflow-hidden">
                            <img class="min-h-full object-cover" src="https://d1pnnwteuly8z3.cloudfront.net/images/a4f01840-cd76-49a6-9d2c-aded32ed05e1/a6926183-4c3d-46bb-9ad1-e34178b3bcf9.webp" loading="lazy" width="1063" height="649" alt="" />
                        </div>
                    </div>
                    <div class="col-span-3 lg:col-span-1 flex flex-col gap-y-8">
                        <div>
                            <div class="block relative group overflow-hidden">
                                <img class="" src="https://d1pnnwteuly8z3.cloudfront.net/images/a4f01840-cd76-49a6-9d2c-aded32ed05e1/c00b53a9-f2c3-4001-b159-a3a1620cb641.webp" loading="lazy" width="1062" height="649" alt="" />
                            </div>
                        </div>
                        <div>
                            <div class="block relative group overflow-hidden">
                                <img class="" src="https://d1pnnwteuly8z3.cloudfront.net/images/a4f01840-cd76-49a6-9d2c-aded32ed05e1/80f090de-9139-49f4-b94c-bbcbaf562dbb.webp" loading="lazy" width="1062" height="648" alt="" />
                            </div>
                        </div>
                    </div>
                </div>
                <div class="flex justify-end mt-2 md:mt-8">
                    <a class="btn group p-0 font-medium" href="#">
                        <span>View all projects</span>
                        <svg class="fas w-6 duration-300 ml-3 group-hover:ml-4" width="100%" viewBox="0 0 25 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M24.5303 6.53033C24.8232 6.23744 24.8232 5.76256 24.5303 5.46967L19.7574 0.696699C19.4645 0.403806 18.9896 0.403806 18.6967 0.696699C18.4038 0.989593 18.4038 1.46447 18.6967 1.75736L22.9393 6L18.6967 10.2426C18.4038 10.5355 18.4038 11.0104 18.6967 11.3033C18.9896 11.5962 19.4645 11.5962 19.7574 11.3033L24.5303 6.53033ZM0 6.75H24V5.25H0V6.75Z" fill="currentcolor"></path>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="py-16 bg-primary-50 lg:py-32">
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="max-w-[36rem] mx-auto text-center mb-6 md:mb-10 lg:md-12">
                    <p class="mb-4 text-gray-700">Features</p>
                    <h2 class="h2 mb-4">Design that solves problems, one product at a time</h2>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-6 gap-y-6">
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/b3bfff48-7942-4103-b866-62c401cab00b.svg" width="32" height="28" alt="" />
                        <h3 class="h5 font-medium">Get everything in one place</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/aa566fc9-af17-4ce7-b1f6-beabfb16b6ff.svg" alt="" width="32" height="32" />
                        <h3 class="h5 font-medium">Easy sizing</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/9ceb8efb-9d33-4930-bddb-8e63c3d5a33e.svg" alt="" width="35" height="35" />
                        <h3 class="h5 font-medium">Steep discounts</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/919c7416-bcd6-4e10-bf9d-2233a9c63289.svg" alt="" width="35" height="35" />
                        <h3 class="h5 font-medium">AI Style advisor</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/aa566fc9-af17-4ce7-b1f6-beabfb16b6ff.svg" alt="" width="32" height="32" />
                        <h3 class="h5 font-medium">No more wasted time</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                    <div class="bg-white p-6 md:px-12 md:py-8">
                        <img class="mb-4" src="https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/9409090c-4977-435d-8a41-8edaef1a8cb4.svg" alt="" width="34" height="34" />
                        <h3 class="h5 font-medium">Ease of use</h3>
                        <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="py-16 bg-neutral lg:py-32">
    <div class="container">
        <div class="row gap-y-6">
            <div class="col md:w-4/12">
                <h2 class="h3 mb-4">What our clients say about us</h2>
                <p class="text-muted">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
            <div class="col md:w-8/12">
                <div class="swiper-container relative">
                    <div class="swiper relative" data-toggle="swiper" data-options="{'loop': true,'slidesPerView':1,'test':true,'pagination':{'el':'.swiper-pagination','clickable':true,'renderBullet':'number','bulletClass':'swiper-pagination-bullet w-8 h-8 flex justify-center items-center text-base text-center text-dark opacity-100 bg-tertiary-300/40 rounded-full cursor-pointer','bulletActiveClass':'swiper-pagination-bullet-active bg-tertiary-600 text-white'},'spaceBetween':16,'breakpoints':{'1024':{'slidesPerView':1,'slidesPerGroup':1}},'navigation':{'prevEl':'.swiper-btn-prev','nextEl':'.swiper-btn-next'}}">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide">
                                <div class="min-h-64 px-4">
                                    <p class="text-2xl font-medium leading-normal">valami ilyesmihez mit szolnatok?</p>
                                    <div class="mt-16 flex gap-4"></div>
                                </div>
                            </div>
                            <div class="swiper-slide">
                                <div class="min-h-64 px-4">
                                    <p class="text-2xl font-medium leading-normal">"Working with this agency has been a very positive experience. They really know what they are doing. I am extremely satisfied!"</p>
                                    <div class="mt-16 flex gap-4">
                                        <div class="w-12 h-12 bg-[url('https://d1pnnwteuly8z3.cloudfront.net/images/dafc1e05-b0e8-4c6d-b375-4a62333bbd5a/467a03a8-c095-4d13-827a-ee33dd8ca04a.png')] bg-cover bg-center rounded-full"></div>
                                        <div>
                                            <div class="text-muted">John Williams</div>
                                            <div class="text-sm text-muted">Co-founder</div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="absolute bottom-2 right-2 z-[999] flex gap-2"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<section class="py-16 lg:py-32">
    <div class="container">
        <div class="row gap-y-12">
            <div class="col md:w-4/12">
                <h2 class="h3 mb-4">Frequently asked questions</h2>
            </div>
            <div class="col md:w-8/12">
                <div class="accordion">
                    <div class="accordion-item">
                        <button class="accordion-header" data-toggle="accordion" aria-expanded="false">
                            <span class="w-8 md:mr-8 text-secondary">01</span>Kerdes1
                        </button>
                        <div class="accordion-collapse hidden">
                            <div class="accordion-body md:ml-16">
                                <p class="text-muted mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                            </div>
                        </div>
                    </div>
                    <div class="accordion-item">
                        <button class="accordion-header" data-toggle="accordion" aria-expanded="false">
                            <span class="w-8 md:mr-8 text-secondary">02</span>Kerdes2
                        </button>
                        <div class="accordion-collapse hidden">
                            <div class="accordion-body md:ml-16">
                                <p class="text-muted mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                            </div>
                        </div>
                    </div>
                    <div class="accordion-item">
                        <button class="accordion-header" data-toggle="accordion" aria-expanded="false">
                            <span class="w-8 md:mr-8 text-secondary">03</span> Kerdes3
                        </button>
                        <div class="accordion-collapse hidden">
                            <div class="accordion-body md:ml-16">
                                <p class="text-muted mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                            </div>
                        </div>
                    </div>
                    <div class="accordion-item">
                        <button class="accordion-header" data-toggle="accordion" aria-expanded="false">
                            <span class="w-8 md:mr-8 text-secondary">04</span> Kerdes4
                        </button>
                        <div class="accordion-collapse hidden">
                            <div class="accordion-body md:ml-16">
                                <p class="text-muted mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                            </div>
                        </div>
                    </div>
                    <div class="accordion-item">
                        <button class="accordion-header" data-toggle="accordion" aria-expanded="false">
                            <span class="w-8 md:mr-8 text-secondary">05</span> Kerdes4
                        </button>
                        <div class="accordion-collapse hidden">
                            <div class="accordion-body md:ml-16">
                                <p class="text-muted mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
<footer class="pt-16 lg:pt-32 bg-primary" id="footer">
    <div class="container text-white">
        <div class="row">
            <div class="col w-6/12">
                <a class="navbar-brand text-white mb-12" href="/"></a>
                <h1 class="text-muted">StyleSwipe</h1>
            </div>
            <div class="col w-6/12">
                <div class="flex gap-4">
                    <a href="https://facebook.com" class="text-white" target="_blank">
                        <i class="text-2xl fab fa-facebook fa-3x"></i>
                    </a>
                    <a href="https://twitter.com" class="text-white" target="_blank">
                        <i class="text-2xl fab fa-twitter fa-3x"></i>
                    </a>
                    <a href="https://instagram.com" class="text-white" target="_blank">
                        <i class="text-2xl fab fa-instagram fa-3x"></i>
                    </a>
                    <a href="https://linkedin.com" class="text-white" target="_blank">
                        <i class="text-2xl fab fa-linkedin fa-3x"></i>
                    </a>
                </div>
            </div>
        </div>
    </div>
</footer>