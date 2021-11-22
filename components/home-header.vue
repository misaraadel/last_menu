<template>
<nav class="w-full absolute top-0 left-0 z-full-max pt-6">
   <div class="container">
      <div class="content w-full flex justify-between items-center content-center">
         <coreLogo /> 
         
         <ul class="navbar-nav flex flex-row items-center content-center">
            <template v-for="nav in navs" :key="nav.img">
               <li class="ml-7">
                  <a :href="`${nav.link}`" class="link-content flex items-center content-center">
                     <img
                        :src="`/img/${nav.img}.svg`"
                        class="w-navIcon h-navIcon object-contain ml-2"
                        :alt="`${alt}`" />

                     <span class="text-paragraph font-normal leading-paragraph text-white">
                        {{ nav.title }}
                     </span>
                  </a>
               </li>
            </template>
         </ul>
         
         <coreCall-to-action 
            btnClass="secondary"
            img="primary"
            textColor="text-primary" />
      </div>
   </div>
</nav>
</template>

<script setup lang="ts">
   import { ref } from 'vue'

   const alt = 'بدات خدمات المنيو.كوم في عام ٢٠٠٧ وهدفنا هو تأسيس وتطوير مطاعم الوجبات السريعة من البداية الي النجاح، من خلال فريق متخصص في إدارة وتشغيل مطاعم الوجبات السريعة والكوفي شوب'

   const navs = ref([{

         link: '#intro',
         img: 'home',
         title: 'الرئيسية',
      
      },{
      
         link: '#about',
         img: 'about',
         title: 'عن المينيو'
      
      },{

         link: '#menu',
         img: 'menu',
         title: 'منيو المطاعم'
      
      },{
         link: '#services',
         img: 'services',
         title: 'الخدمات'
      }
   ])
</script>

<style lang="scss">
nav{
   .link-content{
      
      &:hover{
         span{
            color: #EBA40C;
         }
      }
   }
}

@media (max-width: 700px) {
nav{  

   .brand-name{
      width: 140px;
   }   

   .navbar-nav{
      width: 100%;
      position: fixed;
      bottom: 0;
      left: 0;
      z-index: 9999 !important;
      justify-content: center;
      background-color: #3F0366;
      padding: 10px 0px 4px 0px;
      box-shadow: 0px 0px 10px rgba($color: #EBA40C, $alpha: .4);

      li{
         margin: 0px;
         width: calc(100% / 4);

         .link-content{
            flex-direction: column;
            justify-content: center;
            text-align: center;
            
            img{
               margin: 0px !important;
            }

            span{
               font-size: 10px;
            }
         }
      }
   }
}
}
</style>
