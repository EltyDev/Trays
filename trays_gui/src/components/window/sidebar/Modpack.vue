<script setup lang="ts">
    import { ref } from "vue";
    const show = ref(false);

    const props = defineProps<{
        name: string,
        icon: string,
        background: string
    }>();

</script>

<template>
    <div class="modpack" @mouseenter="show = true" @mouseleave="show = false">
        <img :src=background class="modpack-background"/>
        <div class="modpack-left">
            <img :src=icon class="modpack-icon"/>
            <div class="modpack-text">
                <transition name="fade">
                    <h3>{{ name }}</h3>
                </transition>
                <p v-if="show">click to view modpack</p>
            </div>
        </div>
        <transition name="fade">
            <div v-if="show" class="modpack-button-container">
                <svg class="modpack-button" width="30" height="33" viewBox="0 0 30 33" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g filter="url(#filter0_d_31_21)" transform="matrix(1, 0, 0, 1, -0.000005, 4.000013)">
                        <path d="M24.7855 10.4813L7.59796 0.320182C6.20148 -0.505014 4.06281 0.295768 4.06281 2.33678V22.6542C4.06281 24.4852 6.05011 25.5887 7.59796 24.6708L24.7855 14.5145C26.3187 13.6112 26.3235 11.3846 24.7855 10.4813Z" fill="white"/>
                    </g>
                    <defs>
                        <filter id="filter0_d_31_21" x="0.0628052" y="-0.000518799" width="29.8744" height="33.001" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                        <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                        <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                        <feOffset dy="4"/>
                        <feGaussianBlur stdDeviation="2"/>
                        <feComposite in2="hardAlpha" operator="out"/>
                        <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>
                        <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_31_21"/>
                        <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_31_21" result="shape"/>
                        </filter>
                    </defs>
                </svg>
            </div>
        </transition>
    </div>
</template>

<script lang="ts">
</script>

<style scoped>

    .fade-enter-active, .fade-leave-active {
    transition: opacity .5s
    }
    .fade-enter, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
    opacity: 0
    }
    .modpack {
        position: relative;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        background-size: cover;
        background-position: center;
        box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25); 
        border-radius: 1.25em; 
        padding: 0.625em 0.938em; 
    }

    .modpack-left {
        display: flex;
        justify-content: center;
        align-items: center
    }

    .modpack-background {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
        border-radius: 1.25em;
        filter: blur(0.181em) !important;
    }

    .modpack-text {
        display: flex;
        flex-direction: column;
        margin-left: 0.625em;
        justify-content: center;
    }

    .modpack-text > h3 {
        font-weight: 600;
        font-size: 1.875em;
        text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25); 
        margin: 0;
    }

    .modpack-text > p {
        font-weight: 400;
        font-size: 0.938em;
        margin: 0;
    }

    .modpack-button {
        margin: 0;
        filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25)) !important;
        padding: 0;
        border: none;
    }

    .modpack-icon {
        width: 4.375em;
        height: 4.375em;
    }

    .modpack-button-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 3.750em;
        height: 3.750em;
        border-radius: 1.375em;
        background: #904BC7;
        cursor: pointer;
        box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.50);
    }
</style>