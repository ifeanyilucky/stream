<template>
    <div ref="sectionWrapper">


        <section class="section1 py-5" ref="section1">
            <div class="container my-5 py-5">
                <div class="row align-items-center">
                    <div class="col-md-6">
                        <h2 class="display-5">All your streams in one place</h2>
                        <p class="text-muted my-4">Manage your incoming and outgoing streams.<br /> You can start, edit and
                            stop
                            each
                            stream with just a few
                            clicks.</p>
                        <button class="button">Early Access</button>
                    </div>
                    <div class="col-md-6">
                        <img src="/static/images/community_money.png" class="img-fluid w-100" />
                    </div>
                </div>
            </div>
        </section>
        <section class="section2 py-5" ref="section2">
            <div class="container my-5 py-5">
                <div class="row align-items-center">
                    <div class="col-md-6">
                        <CodeDocs />
                    </div>
                    <div class="col-md-6 docs-cta">
                        <h2 class="display-5">Build with streams</h2>
                        <div class=" my-4">
                            <p>
                                With Streamroan, you can open a stream with a single line of code. Plus, thanks to our SDK
                                Suite
                                and Protocol Docs, you'll have everything you need to integrate asset streaming into your
                                apps.
                            </p>
                            <p class="my-4">
                                Need to debug? We've got you covered with the Streamroan Console to make it as easy as
                                possible.
                            </p>
                        </div>
                        <button class="button button-white">Protocol Docs Demo</button>
                    </div>
                </div>
            </div>
        </section>
        <LandingExplore />
    </div>
</template>


<script lang="ts">
// eslint-disable-next-line @typescript-eslint/ban-ts-comment
// @ts-nocheck
import { ref } from 'vue';
import { ScrollTrigger } from 'gsap/all';
import gsap from "gsap";
import LandingExplore from './LandingExplore.vue';
import CodeDocs from "./CodeDocs.vue"
gsap.registerPlugin(ScrollTrigger);




export default {
    name: 'CallToAction',
    components: {
        LandingExplore,
        CodeDocs
    },
    data() {
        return {
            section1Ref: ref(null),
            section2Ref: ref(null),
            sectionWrapper: ref(null),

        };
    },
    mounted() {
        this.section2Ref = this.$refs.section2
        this.sectionWrapper = this.$refs.sectionWrapper
        console.log(this.section2Ref)
        gsap.to(this.section2Ref, {
            scrollTrigger: {
                trigger: this.section2Ref,
                start: 'top center',
                end: 'bottom center',
                onEnter: () => gsap.to(this.sectionWrapper, { backgroundColor: 'rgb(33, 37, 58)' }),
                onLeaveBack: () => gsap.to(this.sectionWrapper, { backgroundColor: '#fff' }),
                onEnterBack: () => gsap.to(this.sectionWrapper, { backgroundColor: 'rgb(33, 37, 58)' }),
                onLeave: () => gsap.to(this.sectionWrapper, { backgroundColor: '#fff' }),

            }
        })
    },
}
</script>

<style lang="scss" scoped>
.section1 {
    height: 100%;
    display: flex;
    align-items: center;
}

.section2 {
    height: 100%;
    display: flex;
    align-items: center;
    color: #fff !important
}

.docs-cta {
    @media(max-width: 768px) {

        text-align: center;
        margin-top: 2rem;
    }

}
</style>