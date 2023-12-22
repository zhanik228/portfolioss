<template>
    <section class="containerr mx-auto flex flex-col sm:flex-row justify-between items-center gap-4">
        <div class="flex flex-col items-start gap-2 max-w-[537px] my-2">
            <h2 class="text-2xl">{{ $t('intro.intro-title.author') }}
            {{  $t('intro.intro-title.text') }}
            <span class="text-[#C778DD]">
                {{ $t('intro.intro-title.first-profession') }}
            </span>
            {{ $t('intro.intro-title.and') }}
            <span class="text-[#C778DD]">
                {{ $t('intro.intro-title.second-profession') }}
            </span>
            </h2>
            <p class="text-[#ABB2BF]">{{ $t('intro.intro-description') }}</p>
            <primary-button>
                {{ $t('intro.contact-me') }}
            </primary-button>
        </div>
        <div class="relative">
            <img 
                class="absolute z-[-1] top-[19%] left-0"
                src="../assets/Logopurple.svg" 
                alt="purple logo">
            <img
                class="absolute bottom-[20%] right-5" 
                src="../assets/Dots.svg" 
                alt="dots"
            >
            <img class="block w-full" src="../assets/Image.png" alt="intro img">
            <p class="flex items-center gap-2 p-2 border">
                <span 
                    class="block bg-[#C778DD] w-4 h-4"
                ></span>
                <span class="text-[#ABB2BF]">
                    {{ $t('intro.current-work-prefix') }}
                </span>
                <span>
                    {{ $t('intro.current-work') }}
                </span>
            </p>
        </div>
    </section>
</template>

<script>
import PrimaryButton from '@/components/button/PrimaryButton.vue'

export default {
    components: {
        PrimaryButton
    }
}
</script>

<style>
.quota {
    position: relative;
    top: -5px;
    width: 41px;
    background: #282C33;
    height: 28px;
}

.quota::before {
    content: '';
    position: absolute;
    top: 0;
    display: block;
    width: 10px;
    height: 10px;
    background-color: gray;
    border-radius: 50%;
}

.quota::after {
    content: '';
    position: absolute;
    top: -10px;
    left: 5px;
    display: block;
    border: 7px solid gray;
    background-color: gray;
    transform: rotate(30deg);
    border-left: none;
}

.quota-section {
    position: relative;
}

.quota-section::after {
    content: '';
    position: absolute;
    top: 30px;
    right: 0;
    border: 1px solid white;
    border-right: 0;
    width: 80px;
    height: 100px;
}

@media screen and (max-width: 925px) {
    .quota-section::after {
        display: none;
    }
}
</style>