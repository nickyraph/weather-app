<script >

import CloudyIcon from './icons/CloudyIcon.vue';
import Gradient from './icons/Gradient.vue';
import moment from 'moment';

export default {
    props: ['city'],

    data(){
        return {
            url: 'https://api.openweathermap.org/data/2.5/weather?q=' + this.city + '&units=metric&appid=b4553061313b2452476c48ca235a4d96',
            temp: null,
            wind_speed: null,
            condition: null,

            date: moment().format('dddd: H:mm')
        }
    },

    methods: {
        async fetchData(){
            const response = await fetch(this.url);

            const data = await response.json();

            this.temp = data.main.temp;

            this.wind_speed = data.wind.speed;

            this.condition = data.weather[0].main

            console.log(data)
        
        }
    },

    mounted(){

        this.fetchData();

    },

    components : {
        CloudyIcon, Gradient
    }

}

</script>

<template>

    <div class="py-5 px-3 bg-[#24353E] max-w-lg rounded-lg relative">
        <div class="icon">
            <div class="absolute top-0 -translate-y-1/2 w-80 -right-1/3">
                <CloudyIcon />
            </div>
        </div>
        <div class="space-y-6 px-8 text-white mt-24 mb-6">
            <h3 class="text-2xl font-bold"> {{ city }} <span class="font-light ml-5">{{ this.temp }}<sup>o</sup>C</span></h3>
            <span class="block">Wind speed: {{ this.wind_speed }} km</span>
            <span class="block">{{ this.date }}</span>
            <span class="block">{{ this.condition }}</span>
        </div>

        <div class="absolute top-0 right-0 w-80 -translate-y-20 translate-x-16">
            <Gradient />
        </div>
    </div>
</template>
