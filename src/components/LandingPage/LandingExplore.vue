
<template>
    <section>
        <div class="container h-100">
            <div class="wrapper h-100">
                <div class="row align-items-center justify-content-center h-100">
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
                    </div>
                </div>
                <div class="featured-wrapper">

                    <div class="logo-wrapper one" v-for="company in companies" :key="company.about">
                        <img alt="--" :src="company.logo" />
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script lang="ts">

const companies = [
    {
        logo: '/static/logo/flutterwave.png',
        url: '',
        title: 'Flutterwave',
        about: '',
    },
    {
        logo: '/static/logo/grey.webp',
        url: '',
        title: 'Grey Finance',
        about: '',
    },
    {
        logo: '/static/logo/kuda.png',
        url: '',
        title: 'Kuda Bank',
        about: '',
    },
    {
        logo: '/static/logo/paystack.png',
        url: '',
        title: 'Paystack',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
    {
        logo: '/static/logo/thebrik.png',
        url: 'https://thebrik.co',
        title: 'Thebrik Co',
        about: '',
    },
]

export default {
    name: 'LandingExplore',
    data() {
        return {
            companies
        }
    }
}
</script>
<style lang="scss" scoped>
section {
    height: 100vh;
    position: relative;
}

.wrapper {
    z-index: 9999;
}

.featured-wrapper {
    position: absolute;
    left: 50%;
    top: 50%;
    width: 1572px;
    height: 861px;
    padding: 0px;
    margin: -430.5px 0px 0px -786px;
    overflow: inherit;

    @media (min-width: 768px) {
        .logo-wrapper {
            position: absolute;
            top: 0px;
            left: 0px;
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
        margin: 0px;
        padding: 35px;
        border-radius: 92px;
        background-color: rgb(242, 245, 253);
        display: flex;
        align-items: center;

        img {
            height: auto;
            width: 100%;
        }

        :nth-child(2) {
            margin: 0px 0px 0px 485px;
        }

        :nth-child(3) {
            margin: 0px 0px 0px 485px;
        }

        :nth-child(4) {
            margin: 5px 0px 0px 775px;
        }

        :nth-child(5) {
            margin: 15px 0px 0px 1096px;
        }

        :nth-child(6) {
            margin: 300px 0px 0px 1035px;
        }

        :nth-child(7) {
            margin: 230px 0px 0px 1322px;
        }

        :nth-child(8) {
            margin: 0px 0px 0px 485px;
        }

        :nth-child(9) {
            margin: 620px 0px 0px 760px;
        }

        :nth-child(10) {
            margin: 300px 0px 0px 1035px;
        }

        :nth-child(11) {
            margin: 601px 0px 0px 196px;
        }

        :nth-child(12) {
            margin: 309px 0px 0px;
        }

    }


    .logo-wrapper.three {
        margin: 0px 0px 0px 485px;
    }

    .logo-wrapper.four {
        margin: 5px 0px 0px 775px;
    }

    .logo-wrapper.five {
        margin: 15px 0px 0px 1096px;
    }

    .logo-wrapper.six {
        margin: 300px 0px 0px 1035px;
    }

    .logo-wrapper.seven {
        margin: 230px 0px 0px 1322px;
    }

    .logo-wrapper.eight {
        margin: 555px 0px 0px 1040px;
    }

    .logo-wrapper.nine {
        margin: 620px 0px 0px 760px;
    }

    .logo-wrapper.ten {
        margin: 300px 0px 0px 1035px;
    }

    .logo-wrapper.eleven {
        margin: 601px 0px 0px 196px;
    }

    .logo-wrapper.twelve {
        margin: 309px 0px 0px;
    }




}
</style>