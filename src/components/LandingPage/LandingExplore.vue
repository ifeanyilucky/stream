
<template>
    <section ref="section">
        <div class="container">
            <div class="wrapper">
                <div class="row align-items-center justify-content-center">
                    <div class="col-md-6 col-12 text-center mx-auto">
                        <h3 class="display-4">
                            Explore our growing ecosystem
                        </h3>
                        <p class="text-muted my-4">
                            From real-time investing to crypto-native subscriptions and more, our community of developers
                            and
                            partners is leveraging Superfluid to build unique, powerful financial experiences.
                        </p>
                        <button class="button">Explore now</button>


                        <div class="featured-wrapper" ref="featuredWrapper">

                            <a :href="company.url" class="logo-wrapper" v-for="company in companies" :key="company.about"
                                ref="featured" :style="[{ backgroundColor: company.color }]"
                                @mouseover="open = company.title" @mouseout="open = 0">
                                <div v-if="open = company.title" style="text-align: left" class="info">
                                    <img :src="company.logo" class="small-logo" size="30%" :alt="company.title" />
                                    <h5>{{ company.title }}</h5>
                                    <p class="small">{{ company.about }}</p>
                                </div>

                                <img alt="--" class="large-logo" :src="company.logo" />


                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script lang="ts">
// eslint-disable-next-line @typescript-eslint/ban-ts-comment
// @ts-nocheck
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/all'
gsap.registerPlugin(ScrollTrigger)

const companies = [
    {
        logo: '/static/logo/flutterwave.png',
        url: 'https://flutterwave.com',
        title: 'Flutterwave',
        about: 'Sell online, process payments, build financial products, or use business tools designed to grow your business.',
        color: 'rgb(255, 179, 179)'
    },
    {
        logo: '/static/logo/grey.webp',
        url: 'https://grey.co',
        title: 'Grey Finance',
        about: 'Open a global bank account in minutes for free. Join over 100,000 African freelancers and remote workers and send payments,',
        color: 'rgb(169, 169, 169)'
    },
    {
        logo: '/static/logo/kuda.png',
        url: 'https://kuda.com',
        title: 'Kuda Bank',
        about: 'Kuda, the money app for Africans licensed by the CBN. Zero maintenance fees, free transfers, automatic savings & investments.',
        color: 'rgb(255, 247, 232)'
    },
    {
        logo: '/static/logo/paystack.png',
        url: 'https://paystack.com',
        title: 'Paystack',
        about: 'Modern online and offline payments for Africa',
        color: 'rgb(242, 245, 253)'
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: 'Thebrik is the complete hostel rental solution for agents and university students - list a hostel, rent a hostel.',
        color: 'rgb(222, 222, 255)'
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: 'Thebrik is the complete hostel rental solution for agents and university students - list a hostel, rent a hostel.',
        color: 'rgb(222, 222, 295)'
    },


]

export default {
    name: 'LandingExplore',
    data() {
        return {
            companies,
            open: 'Thebrik',
        }
    },
    mounted() {
        const sectionRef = this.$refs.section;
        const featuredRef = this.$refs.featured;

        gsap.to(featuredRef, {
            xPercent: -100 * (featuredRef.length - 1),
            ease: 'none',
            scrollTrigger: {
                trigger: sectionRef,
                pin: true,
                end: '+=3000',
                scrub: 1,

            }
        })
    },
    methods: {
        openCompanyInfo() {
            console.log('hovered sucessfully')
        }
    }
}
</script>
<style lang="scss" scoped>
section {
    height: 100%;
    position: relative;
}

.wrapper {
    z-index: 9999;
}

.featured-wrapper {


    padding: 0px;
    display: flex;
    flex-flow: row;
    margin: 3rem 0;

    /* overflow: inherit; */

    @media (min-width: 768px) {
        .logo-wrapper {

            max-width: 250px;
            height: 239px;
            flex: 1 0 250px;
            margin: 0px;
            padding: 35px;
            border-radius: 92px;
        }
    }

    .logo-wrapper {
        max-width: 250px;
        height: 239px;
        flex: 1 0 250px;
        margin: 0 10px;
        padding: 35px;
        border-radius: 92px;
        display: flex;
        align-items: center;
        transition: 0.3s all ease-in-out;
        cursor: pointer;
        text-decoration: none;
        color: #000;

        img {
            height: auto;
            width: 100%;
        }

        &:hover {
            border-radius: 75px;


        }

        &:hover .large-logo {
            display: none;
        }

        .info {
            display: none;

        }

        &:hover .info {
            display: block !important;
        }

    }






}
</style>