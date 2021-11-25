<template>
  <footer class="w-full pt-14 pb-2 bg-no-repeat">
    <div class="container py-4">
      <div class="grid lg:grid-cols-3 md:grid-cols-1 sm:grid-cols-1 lg:gap-36 md:gap-12 sm:gap-9 gap-9">
        <div class="content">
          <coreLogo />

          <p class="mt-9 text-justify text-copyrights font-normal leading-footer text-white">
            {{ footerDesc }}
          </p>
        </div>

        <div class="content ">
          <h4 class="font-bold mb-9 text-secondary text-services leading-footer">
            {{ footerCategory }}
          </h4>

          <div class="flex data-link items-start content-start">
            <ul>
              <li>
                <a href="#intro" class="text-copyrights font-normal text-white leading-head">
                  الرئيسية
                </a>
              </li>

              <li>
                <a href="#about" class="text-copyrights font-normal text-white leading-head">
                  عن المينيو
                </a>
              </li>

              <li>
                <a href="#services" class="text-copyrights font-normal text-white leading-head">
                  الخدمات
                </a>
              </li>

              <li>
                <a href="#menu" class="text-copyrights font-normal text-white leading-head">
                  منيو المطاعم
                </a>
              </li>

              <li>
                <a href="#help" class="text-copyrights font-normal text-white leading-head">
                  كيف يساعدك فريق المنيو ؟
                </a>
              </li>
            </ul>

            <ul>
              <li class="mb-1">
                <a href="#contact" class="text-copyrights font-normal text-white leading-head">
                  أطلب خدمتك
                </a>
              </li>
            </ul>
          </div>
        </div>

        <div class="content">
          <h4 class="font-bold mb-9 text-secondary text-services leading-footer">
            {{ footerContact }}
          </h4>

          <ul>
            <li class="pb-5 border-b border-solid border-white border-opacity-10">
              <a href="#" class="flex items-center content-center">
                <img 
                  src="/img/footer_location.svg" 
                  class="w-navIcon h-navIcon object-contain ml-4"
                  :alt="`${footerDesc}`" />

                <span class="text-copyrights font-bold leading-head text-white">
                  المملكة العربية السعودية
                </span>
              </a>
            </li>

            <li class="py-5 border-b border-solid border-white border-opacity-10">
              <a href="#" class="flex items-center content-center">
                <img 
                  src="/img/message.svg" 
                  class="w-navIcon h-navIcon object-contain ml-4"
                  :alt="`${footerDesc}`" />

                <span class="text-copyrights font-bold leading-head text-white">
                  info@el-menu.com
                </span>
              </a>
            </li>

            <li class="pt-5">
              <a @click="callus()" class="flex cursor-pointer items-center content-center">
                <img 
                  src="/img/footer_call.svg" 
                  class="w-navIcon h-navIcon object-contain ml-4"
                  :alt="`${footerDesc}`" />

                <span class="text-copyrights font-bold leading-head text-white">
                  00966546666174
                </span>
              </a>
            </li>
          </ul>
        </div>
      </div>

      <div class="heading-content w-full mt-9 mb-5 relative z-max">
        <h4 class="text-copyrights bg-primary px-12 text-secondary font-normal leading-paragraph relative w-fit-content m-auto">
          {{ socailMedia }}
        </h4>
      </div>
      
      <coreSocial-media class="w-full justify-center" />
    </div>
  </footer>
</template>

<script setup lang="ts">
const { callus  } = useActions()

const footerDesc = 'بدات خدمات المنيو.كوم في عام ٢٠٠٧ وهدفنا هو تأسيس وتطوير مطاعم الوجبات السريعة من البداية الي النجاح، من خلال فريق متخصص في إدارة وتشغيل مطاعم الوجبات السريعة والكوفي شوب'

const socailMedia = 'تابعنا على'

const footerCategory = 'أقسام المنيو'

const footerContact = 'تواصل معنا'
</script>

<style lang="scss">
footer{
  
  .data-link{
    ul {
      li{
        margin-bottom: 10px;

        &:last-child{
          margin: 0px;
        }
      }
    }  
  }

  .heading-content{
    &::after{
      content: '';
      position: absolute;
      width: 100%;
      height: 1px;
      background-color: rgba($color: #fff, $alpha: .10);
      top: 50%;
      left: 0px;
      transform: translateY(-50%);
      z-index: -1;
    }
  }
}
</style>


