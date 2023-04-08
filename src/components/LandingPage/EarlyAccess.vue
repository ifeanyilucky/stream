
<template>
    <section>
        <div class="container h-100">
            <div class="wrapper h-100">
                <div class="row align-items-center justify-content-center h-100">
                    <div class="col-md-6 col-12 text-center mx-auto">
                        <h3 class="display-4">
                            Sign up for early access
                        </h3>
                        <p class="text-muted my-4">
                            Sign up to the Superfluid Flow early access and stay up to date with Superfluid Protocol and the
                            innovative projects building on top of it.
                        </p>
                        <form class="early-access-form">
                            <input type="text" placeholder="Full name" />
                            <input type="email" placeholder="Email" />
                            <button type="submit" class="button">Signup now</button>
                        </form>
                        <p class="text-muted small my-3">By entering your email, you accept our Privacy Policy and Terms of
                            Use.
                        </p>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<script lang="ts">


export default {
    name: 'EarlyAccess',

}
</script>
<style lang="scss" scoped>
section {
    height: 100%;
    padding: 3rem 0;
    position: relative;
}

.early-access-form {
    display: flex;
    flex-flow: column;

    input {
        margin: 10px 0;
        border-radius: 30px;
        border: 1px solid #6c757d;
        padding: 8px 15px;
        outline: none;
    }
}
</style>