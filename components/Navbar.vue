<template>
    <b-navbar :centered="centered" :shadow="shadow">
        <template #brand>
            <b-navbar-item class="brand" tag="router-link" :to="{ path: '/' }">
                Outdoor Vibrations
            </b-navbar-item>
        </template>
        <template #start >
            <b-navbar-item>
                <NuxtLink to="/" class="nav-item">
                    Home
                </NuxtLink>
            </b-navbar-item>
            <b-navbar-item>
                <NuxtLink to="/about" class="nav-item">
                    About
                </NuxtLink>
            </b-navbar-item>
            <b-navbar-item>
                <NuxtLink to="/blogs" class="nav-item">
                    Blog
                </NuxtLink>
            </b-navbar-item>
        </template>

        <template #end>
            
            <b-navbar-item tag="div">
                <NuxtLink to="/subscribe">
                    <div class="buttons">
                        <a class="button">
                            <strong>Subscribe</strong>
                        </a>
                    </div>
                </NuxtLink>
            </b-navbar-item>
        </template>
        <!-- <template #burger></template> -->
    </b-navbar>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            centered: true,
            shadow: true
        }
    }
}
</script>

<style>
nav {
    padding: 0 3.5rem;
}

.nav-item {
    color: black;
}

.brand {
    font-size: 36px;
    font-weight: bold;
}

.brand:hover {
    color: #58B727 !important;
}

a {
    font-size: 18px;
    font-weight: 600;
}

.button {
    background-color: #58b727;
    color: #fff;
}
</style>