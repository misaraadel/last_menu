<template>
<section class="services py-20 relative z-max" id="services">
    <div class="container">
        <coreDescription-style 
            class="text-center lg:w-semi-half md:w-full sm:w-full mx-auto"
            headingStyle="text-primary leading-heading"
            :headContent="`${serviceHead}`"
            descriptionStyle="text-dark mt-2 text-text-paragraph mb-20"
            :description="`${serviceDesc}`"
        />

        <div class="grid lg:grid-cols-3 md:grid-cols-2 sm:grid-cols-1 gap-5">
            <template v-for="service in services" :key="service.img">
                <div class="box w-full overflow-hidden relative z-max flex flex-col justify-center items-center content-center text-center py-12 px-9 bg-white rounded-card">
                    <img 
                        :src="`/img/${service.img}.svg`"
                        class="w-card h-card object-contain"
                        :alt="`${service.title}`" />

                    <h4 class="text-services leading-paragraph my-6 text-dark">
                        {{ service.title }}
                    </h4>

                    <p class="text-paragraph font-normal leading-paragraph text-contact">
                        {{ service.desc }}
                    </p>
                </div>
            </template>
        </div>
    </div>
</section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const services = ref([
    {
        img: 'service_1',
        title: 'تأسيس المطاعم',
        desc: 'نساعدك في تأسيس مطعمك او الكوفي شوب الخاص بك بشكل احترافي، من الفكرة وحتى الافتتاح حتي تتمكن من تأسيس مشروعك خلال إطار زمني محدد وتجنب الكثير من المخاطر.'
    },{
        img: 'service_2',
        title: 'تطوير المطاعم',
        desc: 'نساعدك في إدارة مطعمك بشكل احترافي من خلال المتابعة المستمرة للفروع والاشراف الكامل على جميع عمليات التشغيل داخل المطعم، بالاضافة لوضع الخطة المناسبة لتطوير المشروع وفريق العمل'
    },{
        img: 'service_3',
        title: 'تشغيل المطاعم',
        desc: 'اذا كنت تواجه مشكلة في المبيعات او الأرباح فقد يكون مطعمك بحاجة الى تطوير من اجل تحقيق الاهداف التي تخطط لها. فريق المنيو جاهز لمساعدتك في مواجهة التحديات التي يواجهها مطعمك .'
    },
])

const serviceHead = 'الخدمات'

const serviceDesc = 'تعاني معظم مشاريع المطاعم في البداية من القرارات الخاطئة وغياب الرؤية ، هنا يأتي دورنا .نقدم لك جلسة مجانية لتحليل أعمالك والوصول إلى رؤية  متكاملة قبل البدء في العمل سيحاول مستشارو المطاعم توجيهك في الاتجاه الصحيح حول كيفية المضي قدمًا في مشروعك'
</script>

<style lang="scss">
.services{
    background-color: rgba($color: #3F0366 , $alpha: .02);

    &::after{
        content: '';
        position: absolute;
        width: 143px;
        height: 143px;
        background: url('/img/service_mask.svg');
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        top: 80px;
        right: 0;
        z-index: -1;
    }

    .box{
        transition: all .4s linear;
        box-shadow: 0px 0px 20px rgba($color: #3F0366, $alpha: .03);

        &::after{
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(-38deg,#3F0366 0,#662851 100%);
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: -1;
            transform: scale(1, 0);
            transform-origin: bottom;
            transition: transform 500ms ease;
        }

        &:hover{
            transform: translateY(-10px);
            box-shadow: 0px 0px 20px rgba($color: #3F0366, $alpha: .1);

            img{
                animation: rotation 1s linear;
            }

            &::after{
                transform: scale(1 , 1);
                transform-origin: top !important;
            }

            h4 {
                color: #EBA40C;
            }

            p{
                color: #fff;
            }
        }
    }   
}
</style>