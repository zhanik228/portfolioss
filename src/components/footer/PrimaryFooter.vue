<template>
    <footer class="bg-red border-t pt-5">
        <div class="containerr mx-auto flex justify-between">
                <div class="flex flex-col gap-2">
                <div class="flex gap-5">
                <div class="logo flex gap-2 font-bold">
                    <img src="@/assets/Logo.svg" alt="Logo" width="16">
                    <router-link to="/"><h1>{{ $t('author') }}</h1></router-link>
                </div>
                    <a href="#" class="text-[#ABB2BF]">elias@elias-dev.ml</a>
                </div>
                <p>{{ $t('intro.intro-title.first-profession') + ' ' + $t('intro.intro-title.and') + ' ' + $t('intro.intro-title.second-profession') }}</p>
            </div>
            <div>
                <h2 class="text-2xl">Media</h2>
                <ul class="flex items-center gap-4 h-[64px]">
                    <li class="p-1">
                        <a target="_blank" href="https://github.com/zhanik228">
                            <img width="21" height="20" src="@/assets/Vectorgithub.svg" alt="">
                        </a>
                    </li>
                    <li class="p-1">
                        <a target="_blank" href="https://t.me/Lvh2288">
                            <img width="21" height="20" src="@/assets/Vectortelegram.svg" alt="">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <p class="text-[#ABB2BF] block text-center">&copy Copyright 2022. Made by Zhanik</p>
    </footer>
</template>

<style scoped>

</style>