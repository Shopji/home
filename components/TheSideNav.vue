<template>
    <div class="sidenav-container">

        <div v-if="toggleSidebar" class="backdrop" @click="$store.dispatch('nav/toggleSidebar')"></div>

        <transition name="slide-side">
            <div v-if="toggleSidebar" class="sidenav">
                <app-links></app-links>
            </div>
        </transition>

    </div>
</template>

<script>
    import AppLinks from '~/components/appLinks'
    export default {
        components: { AppLinks },
        computed: {
            toggleSidebar() {
                return this.$store.getters['nav/toggleSidebar']
            }
        }
    }
</script>


<style lang="scss" scoped>
    .sidenav-container {
        height: 100%;
        width: 100%;
    }
    .sidenav {
        height: 100%;
        width: 300px;
        background-color: #fff;
        z-index: 10000;
        position: fixed;
        top: 0;
        left: 0;
        box-sizing: border-box;
          box-shadow: 0 0 6px 2px rgb(0 0 0 / 4%);
          border-top: 1px none $color-primary;
          margin-top: 69px;
          object-fit: fill;


            /* width: 100%;
            margin-top: 69px;
            border-top: 1px none #f43397;
            background-color: #fff;
            box-shadow: 0 0 6px 2px rgb(0 0 0 / 4%);
            -o-object-fit: fill;
            object-fit: fill; */
    }
    .backdrop {
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.7);
        z-index: 1000;
        position: fixed;
        top: 0;
        left: 0;
    }
    .slide-side-enter-active,
    .slide-side-leave-active {
        transition: all 0.3s ease-out;
    }
    .slide-side-enter,
    .slide-side-leave-to {
        transform: translateX(-100%);
    }
</style>
