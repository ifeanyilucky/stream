<template>
    <div class="position-relative">
        <div class="wrapper  container" ref="section">
            <h3 class="display-5 my-5">
                Why stream money?
            </h3>
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
// @ts-nocheck
import { ref } from 'vue';
import gsap from "gsap"
import ScrollTrigger from "gsap/ScrollTrigger"
gsap.registerPlugin(ScrollTrigger)

export default {
    name: 'WhyStream',
    mounted() {
        this.cardsRef = this.$refs.card

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
                    description: 'Superfluid Protocol is modular and open source, meaning you can use it to build anything you want!'
                },
            ],

        }
    }
}
</script>
<style lang="scss" scoped>
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

