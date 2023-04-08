<template>
    <div class="position-relative" style="overflow-x: hidden">
        <div class="wrapper  container" ref="section">
            <h3 class="display-5 my-5">
                Why stream money?
            </h3>
            <svg viewBox="0 0 900 10" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M9.89998 6C9.43671 8.28224 7.41896 10 5 10C2.23858 10 0 7.76142 0 5C0 2.23858 2.23858 0 5 0C7.41896 0 9.43671 1.71776 9.89998 4H445.1C445.563 1.71776 447.581 0 450 0C452.419 0 454.437 1.71776 454.9 4H890.1C890.563 1.71776 892.581 0 895 0C897.761 0 900 2.23858 900 5C900 7.76142 897.761 10 895 10C892.581 10 890.563 8.28224 890.1 6H454.9C454.437 8.28224 452.419 10 450 10C447.581 10 445.563 8.28224 445.1 6H9.89998Z"
                    fill="#D9D9D9" />
                <mask id="mask0_0_1" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="900" height="10"
                    ref="maskRef">
                    <path
                        d="M9.89998 6C9.43671 8.28224 7.41896 10 5 10C2.23858 10 0 7.76142 0 5C0 2.23858 2.23858 0 5 0C7.41896 0 9.43671 1.71776 9.89998 4H445.1C445.563 1.71776 447.581 0 450 0C452.419 0 454.437 1.71776 454.9 4H890.1C890.563 1.71776 892.581 0 895 0C897.761 0 900 2.23858 900 5C900 7.76142 897.761 10 895 10C892.581 10 890.563 8.28224 890.1 6H454.9C454.437 8.28224 452.419 10 450 10C447.581 10 445.563 8.28224 445.1 6H9.89998Z"
                        fill="#D9D9D9" />
                </mask>
                <g mask="url(#mask0_0_1)">
                    <rect class="mask" y="-49" height="99" fill="black" />
                </g>
            </svg>
            <div class="card-wrapper" ref="cardWrapper">

                <template v-for="(item, index) in items" :key="index">
                    <div class="row-card my-4" ref="card">
                        <div class="img-wrapper">
                            <img :src="item.image" :alt="item.title" />
                        </div>
                        <div class="card-content p-4">
                            <h2 class="my-3">{{ item.title }}</h2>
                            <p>{{ item.description }}</p>
                        </div>
                    </div>
                </template>
            </div>
        </div>

    </div>
</template>

<script lang="ts">
// eslint-disable-next-line @typescript-eslint/ban-ts-comment
// @ts-nocheck
import { ref } from 'vue';
import gsap from "gsap"
import ScrollTrigger from "gsap/ScrollTrigger"
gsap.registerPlugin(ScrollTrigger)

export default {
    name: 'WhyStream',
    mounted() {
        this.cardsRef = this.$refs.card
        const maskRef = this.$refs.maskRef

        gsap.to(this.cardsRef, {
            xPercent: -100 * (this.cardsRef.length - 1),
            ease: 'none',
            scrollTrigger: {
                trigger: this.$refs.section,
                pin: true,
                scrub: 1,
                end: '+=3000'
            }
        })

        // progress bar animation
        gsap.to(maskRef, {
            width: "100%",
            scrollTrigger: {
                trigger: this.$refs.section,
                start: "top left",
                scrub: 1
            }
        });

    },
    data() {
        return {
            cardsRef: ref(null),
            items: [
                {
                    image: '/static/images/illustration_1.png',
                    title: 'Pay and get paid every seconds',
                    description: 'Receive your salary or DAO rewards in a stream and watch as tokens flow directly into your wallet every second.'
                },
                {
                    image: '/static/images/illustration_2.png',
                    title: 'Invest in real-time with streams',
                    description: 'Purchase and sell crypto assets in real-time by streaming exchangeable tokens.'
                },
                {
                    image: '/static/images/illustration_3.png',
                    title: 'Streaming web3 subscriptions',
                    description: 'Enable users to pay for their web3 subscription with ongoing streams instead of recurring transactions.'
                },
                {
                    image: '/static/images/illustration_4.png',
                    title: 'Build an asset streaming dApp',
                    description: 'Streamroan Protocol is modular and open source, meaning you can use it to build anything you want!'
                },
            ],

        }
    }
}
</script>
<style lang="scss" scoped>
svg {

    width: 50vw;

    .mask {
        width: 0;
    }
}

.wrapper {
    margin-top: 10rem;
}

.card-wrapper {
    display: flex;
    flex-flow: row;
    padding-left: 7em;
}

.row-card {
    background-color: rgb(242, 245, 253);
    border-radius: 30px;
    height: 450px;
    width: 350px;
    min-width: 350px;
    margin: 0 13px;

    .img-wrapper {
        width: 100%;

        img {
            width: 100%;
        }
    }

    /* .card-content {} */
}
</style>

