
<template>
    <nav className="container">
        <div class="nav-wrapper">
            <div class="logo">
                <h2>Superfluid</h2>
            </div>
            <ul class="nav-items " :class="navOpen && 'open'">

                <li class="nav-item"><router-link to="/" class="nav-link">Ecosystem</router-link> </li>
                <li class="nav-item"> <router-link to="/" class="nav-link">Developers</router-link> </li>
                <li class="nav-item"> <router-link to="/" class="nav-link">Blog</router-link></li>
                <li class="nav-item"><router-link to="/" class="nav-link">About</router-link> </li>
                <li class="nav-item"><router-link to="/" class="nav-link">Solutions</router-link> </li>
            </ul>
            <ul class="nav-items-mobile " :style="[!navOpen && { display: 'none' }]" :class="navOpen && 'nav-items-mobile'">

                <li class="nav-item"><router-link to="/" class="nav-link">Ecosystem</router-link> </li>
                <li class="nav-item"> <router-link to="/" class="nav-link">Developers</router-link> </li>
                <li class="nav-item"> <router-link to="/" class="nav-link">Blog</router-link></li>
                <li class="nav-item"><router-link to="/" class="nav-link">About</router-link> </li>
                <li class="nav-item"><router-link to="/" class="nav-link">Solutions</router-link> </li>
            </ul>
            <div class="nav-button" v-on:click="handleNavbar">
                <div style="transform-origin: 1% "
                    :style="[navOpen ? { transform: 'rotate(40deg)' } : { transform: 'rotate(0)' }]" />

                <div :style="[navOpen ? { transform: 'rotate(326deg)' } : { transform: 'rotate(0)' }]" />
            </div>
        </div>
    </nav>
</template>

<script lang="ts">
// eslint-disable-next-line @typescript-eslint/ban-ts-comment
// @ts-nocheck
export default {
    name: 'NavbarLayout',
    data() {
        return {
            navOpen: false
        }
    },
    methods: {
        handleNavbar() {
            console.log(this.navOpen)
            if (this.navOpen === true) {
                this.navOpen = false

            }
            else {
                this.navOpen = true
            }

        }
    }
}
</script>
<style lang="scss" scoped>
.nav-wrapper {
    display: flex;
    flex-flow: row;
    margin-top: 20px;
    align-items: center;

    @media (max-width: 768px) {
        justify-content: space-between;

    }


    .nav-button {
        @media (min-width: 768px) {
            display: none;

        }

        cursor: pointer;
        position: fixed !important;
        top: 30px;
        right: 30px;
        z-index: 999;
        background-color: #fff;
        padding: 5px 15px;

        div {


            height: 2px;
            width: 27px;
            background-color: rgb(0, 0, 0);
            border-radius: 10px;
            margin: 8px 0;
            transition: 0.3s all ease-in-out;




        }

        .opened-button {
            div {
                &:first-child {
                    transform: rotate(45deg);
                    transform-origin: left;
                }

                &:last-child {
                    transform: rotate(320deg);

                }
            }
        }
    }

    @media (min-width: 768px) {
        .nav-items-mobile {
            display: none !important
        }
    }

    @media (max-width: 768px) {
        .nav-items {
            display: none !important;

        }



        .nav-items-mobile {
            flex-flow: column !important;
            z-index: 999;
            position: fixed;
            top: 0;
            height: 100vh;
            background-color: #fff;
            width: 100vh;
            font-size: 28px;
            left: 0;
            list-style-type: none;
            padding-top: 3rem;
        }
    }

    .nav-items {
        display: flex;
        flex-flow: row;
        list-style-type: none;
        align-items: center;



        .nav-item {
            margin: 0 10px;

            .nav-link {

                color: #000;
                text-decoration: none;
                transition: 0.3s all ease-in-out;

                &:hover {
                    text-decoration: underline;
                }
            }
        }

    }

}
</style>