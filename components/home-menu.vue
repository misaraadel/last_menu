<template>
<section class="menu relative z-max w-full py-20 bg-white" id="menu">
    <div class="container">
        <coreDescription-style
            class="text-center"
            headingStyle="text-heading leading-heading"
            descriptionStyle="text-dark mt-2 text-text-paragraph mb-20"
            :description="`${menuDesc}`"
            :headContent="`${menuHeading}`" />
        
        <div class="grid lg:grid-cols-4 md:grid-cols-2 sm:grid-cols-1 gap-7">
            <template v-for="meal in menu" :key="meal.code">
                <div class="box w-meal h-meal flex justify-center content-center items-center text-center relative z-max overflow-hidden rounded-circle">
                    <img 
                        :src="`/img/${meal.img}.jpg`" 
                        class="w-full h-full object-cover object-center absolute top-0 left-0 z-min"
                        :alt="`${meal.title}`" />
                    
                    <h4 class="text-meal text-white font-bold leading-paragraph">
                        {{ meal.title }}
                    </h4>
                </div>
            </template>
        </div>
    </div>
</section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const menu = ref([
    {
        code: '1',
        img: 'menu_1',
        title: 'كوفي شوب'
    },{
        code: '2',
        img: 'menu_2',
        title: 'مطاعم برجر'
    },{
        code: '3',
        img: 'menu_3',
        title: 'إفطار'
    },{
        code: '4',
        img: 'menu_4',
        title: 'إفطار'
    },{
        code: '5',
        img: 'menu_5',
        title: 'فرايد تشيكن'
    },{
        code: '6',
        img: 'menu_6',
        title: 'عصائر فريش'
    },{
        code: '7',
        img: 'menu_7',
        title: 'مطاعم بيتزا'
    },{
        code: '8',
        img: 'menu_8',
        title: 'مطاعم وجبات بحرية'
    }
])

const menuHeading = 'منيو المطاعم'
const menuDesc = 'أنواع المطاعم اللي نسويها'
</script>

<style lang="scss">
.menu{

    &::after{
        content: '';
        position: absolute;
        width: 143px;
        height: 143px;
        background: url('/img/menu_mask.svg');
        background-size: contain;
        background-repeat: no-repeat;
        background-position: left;
        top: 80px;
        left: 0;
        z-index: -1;
    }

    .box{
        &::after{
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: url('/img/meal_mask.png');
            background-size: cover;
            background-repeat: no-repeat;
            top: 0;
            left: 0;
            z-index: 0;
            opacity: 0;
            transition: all .4s linear;
        }

        &:hover{
            &::after{
                animation: sideClip 1s linear;
                opacity: 1;
            }
        }
    }
}

@media (max-width: 800px) {
    .menu{
        .box{
            margin: auto;
        }
    }
}
</style>