<template>
  <section id="footerBottom">
        <div class="container-two d-flex aligne-items-center">
            <div class="footer-bottom-left">
                <button>SIGN-UP NOW!</button>
            </div>
            <div class="footer-bottom-right d-flex justify-content-center">
                <div class="social d-flex aligne-items-center px-4">
                    <h2>FOLLOW </h2>
                    <ul class="d-flex list-style-none">
                        <li v-for="(social, index) in linkSocial" :key="`link-${index}`" class="px-4">
                            <a href="">
                                <img :src="require(`@/assets/${social.src}`)" :alt="social.socialName">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'FooterBottom',
    data(){
        return{
            linkSocial: [
                {
                    socialName: 'Facebook',
                    src: 'footer-facebook.png'
                },
                {
                    socialName: 'Periscope',
                    src: 'footer-periscope.png'
                },
                {
                    socialName: 'Pinterest',
                    src: 'footer-pinterest.png'
                },
                {
                    socialName: 'Twitter',
                    src: 'footer-twitter.png'
                },
                {
                    socialName: 'YouTube',
                    src: 'footer-youtube.png'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/styles/generals';
@import '@/styles/utilities';
@import '@/styles/variables';
    #footerBottom{
        background-color: #303030;
        padding: 40px 0;
    }
    .container-two{
        div{
            width: calc(100% / 2);
        }
        button{
            border: none;
            padding: 20px;
            color: #fff;
            background: transparent;
            font-size: 20px;
            border: 3px solid $color_primary;
        }
        h2{
            font-size: 30px;
            color: $color_primary;
        }
    }
</style>