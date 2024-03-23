<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <v-lazy
    :min-height="200"
    :options="{'threshold':0.5}"
    transition="fade-transition"
    >
        <v-container fluid class="pa-0 ma-0" >
            <v-row class="section-1">
                <div class="pt-16 text-center w-100">
                    <transition name="slide-fade">
                        <h1 class="text-white">
                            The Right Solution
                        </h1>
                    </transition>
                    <transition name="slide-fade">
                        <h1 class="text-white">
                            For Technical Services
                        </h1>
                    </transition>
                    <transition name="slide-fade">
                        <h1 class="text-white">
                            And Support
                        </h1>
                    </transition>
                </div>
            </v-row>
            <v-row class="section-2">
                <div class="text-center w-100">

                </div>
            </v-row>
        </v-container>
    </v-lazy>
</template>

<script>
export default {
    name: 'HomePage'
};
</script>

<style>
    .section-1 {
        background: url('../assets/section1_backgound.jpg');
        background-size: cover;
        height: 250px;
    }
    .section-2 {
        height: 400px;
        background-color: skyblue;
    }
    .slide-fade-enter-active {
        transition: all 0.8s ease-out;
    }

    .slide-fade-enter-from {
        transform: translateX(20px);
        opacity: 0;
    }
</style>