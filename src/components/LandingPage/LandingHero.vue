
<template>
    <div class="hero-video-wrapper">

        <video src="/static/videos/1.mp4" autoplay muted loop class="hero-video"></video>
    </div>
    <div class="container-sm">
        <div class="row pt-5">
            <div class="col-md-7 col-12 mt-5 pt-5">
                <h2 class="display-1">
                    Stream money every second.</h2>
                <p class="text-muted py-3">
                    Superfluid is a revolutionary asset streaming protocol that brings subscriptions, salaries, vesting,
                    and
                    rewards to DAOs and crypto-native businesses worldwide.
                </p>
                <div>
                    <button class="button mr-2">Launch App</button>
                    <button class="button button-outline ml-3">Book Demo</button>
                </div>
            <!-- <div class="d-flex logo-wrapper">
                    <h6 class="text-muted">Trusted by:</h6>
                    <img src="/static/logo/flutterwave.png" class="trust-logo" />
                    <img src="/static/logo/kuda.png" class="trust-logo" />
                    <img src="/static/logo/thebrik.png" class="trust-logo" />
                    <img src="/static/logo/grey.webp" class="trust-logo" />
                    <img src="/static/logo/paystack.png" class="trust-logo" />
                    </div> -->
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.logo-wrapper {
    justify-content: space-between;
    align-items: center;
    position: absolute;
    bottom: 0;

    .trust-logo {
        height: 25px;
        width: 100%;
        margin: 10px;
        filter: grayscale(5);
    }
}

.hero {
    width: 100vw;
    overflow-y: scroll;
}

.hero-video-wrapper {
    position: absolute;
    display: block;
    top: 0px;
    left: 0px;
    z-index: -999;
    bottom: 0px;
    width: 100%;
    height: 100%;
    perspective: 500px;
    overflow: hidden;

    .hero-video {
        will-change: auto;
        transform-origin: 100% 0%;
        translate: none;
        rotate: none;
        scale: none;
        transform: translate3d(0px, 0px, 0px);
        height: 100%;
        width: 100vw;
        z-index: 99999;
        object-position: right top;
        object-fit: contain;
        position: absolute;
    }


    @media (min-width: 1200px) {

        .hero-video {
            width: 100%;
            height: 100%;
            left: 8%;
        }
    }

    @media (min-width: 1024px) {

        .hero-video {
            top: 0px;
        }
    }

    @media (min-width: 768px) {
        .hero-video {
            width: 120%;

            top: 0;
            left: -5%;
        }


    }


}
</style>

<script lang="ts">


export default {
    name: 'LandingHero'

}
</script>