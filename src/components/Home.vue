<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <v-lazy
    class="mt-2"
    :options="{'threshold':0.5}"
    transition="fade-transition"
    >
        <v-container fluid class="pa-0 ma-0">
            <v-row class="section-1">
                <div class="text-center w-100">
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
                <div class="text-center w-100 pt-2">
                    <h1>
                        Services
                    </h1>
                    <v-spacer></v-spacer>
                    <v-row align="start" class="px-16">
                        <v-col v-for="service in services" :key="service.name">
                            <v-sheet style="background-color: whitesmoke;">
                                <v-img :src="service.image" height="200"></v-img>
                                <div class="mt-4"><b>{{ service.name }}</b></div>
                                <div class="mt-8"> {{ service.description }}</div>
                            </v-sheet>
                        </v-col>
                    </v-row>
                </div>
            </v-row>
            <v-row class="section-3">
                <v-row align="start" class="text-center">
                    <v-col>
                        <v-sheet class="mt-4" style="background-color: #78909C; color: white">
                            <p class="text-h4 text-left">FANTOM</p>
                            <p class="text-h4 text-left">CORPORATION</p>
                        </v-sheet>
                    </v-col>
                    <v-col>
                        <v-sheet class="mt-4" style="background-color: #78909C; color: white">
                           <p class="text-h6">ABOUT US</p>
                        </v-sheet>
                    </v-col>
                    <v-col>
                        <v-sheet class="mt-4" style="background-color: #78909C; color: white">
                           <p class="text-h6">Pages</p>
                        </v-sheet>
                    </v-col>
                </v-row>
            </v-row>
        </v-container>
    </v-lazy>
</template>

<script>
export default {
    name: 'HomePage',
    data() {
        return {
            services: [
                { 
                    name: 'SYSTEMS ENGINEERING & INTEGRATION', 
                    image: require('../assets/systems_integration.png'),
                    description: "Fantom provides systems engineering and technical support to our nation’s various Defense and Intelligence Community customers. Our staff ensures both your technical goals and program intent are fully met for both small and large programs in all phases of systems development. Fantom has experience with integrating existing systems with Open Source and commercial off-the-shelf products"
                },
                {
                    name: 'SOFTWARE ENGINEERING',
                    image: require('../assets/software_engineering.png'),
                    description: "Fantom provides best-value software development, systems engineering, analysis, integration services and IT solutions. Fantom is focused on the development and integration of advanced technologies that support our customers needs to ensure our national security."
                }
            ]
        }
    }
};
</script>

<style>
    .section-1 {
        background: url('../assets/section1_backgound.jpg');
        background-size: cover;
        display: block;
        min-height: 250px;
        padding-top: 3em;
    }
    .section-2 {
        height: 500px;
        background-color:whitesmoke;
        display: block;
    }
    .section-3 {
        height:500px;
        background-color: #78909C;
        text-align: center;
        display: block;
    }
    .section-3 .v-row{
        margin-inline: 12em;
    }

    .slide-fade-enter-active {
        transition: all 0.8s ease-out;
    }

    .slide-fade-enter-from {
        transform: translateX(20px);
        opacity: 0;
    }
</style>