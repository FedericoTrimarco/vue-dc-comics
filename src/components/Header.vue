<template>
    <div class="container">
      <div class="img-logo">
        <a href="/">
            <img src="@/assets/dc-logo.png" alt="dc-logo">
        </a>

      </div>

        <nav>
            <ul>
                <li tabindex="0" v-for="(link, index) in linkNav" :key="`link-${index}`">
                    <a href="/">{{ link.linkText }}</a>
                </li>
              
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: 'div',
    data(){
        return{
            linkNav: [
                {
                    linkText: 'CHARATTERS',
                },
                {
                    linkText: 'COMICS',
                },
                {
                    linkText: 'MOVIES',
                },
                {
                    linkText: 'TV',
                },
                {
                    linkText: 'GAMES',
                },
                {
                    linkText: 'COLLECTIBLES',
                },
                {
                    linkText: 'VIDES',
                },
                {
                    linkText: 'FANS',
                },
                {
                    linkText: 'NEWS',
                },
                {
                    linkText: 'SHOP',
                }
            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@import '@/styles/generals';
@import '@/styles/variables';
@import '@/styles/utilities';
div{
    display: flex;
    align-items: center;
    
    .img-logo{
        width: calc(100% / 2);
    }
    nav{
        height: 100%;
        ul{
            height: 100%;
            display: flex;
            li{
                cursor: pointer;
                height: 100%;
                padding: 20px 25px;
                font-size: 20px;
                list-style: none;
                display: flex;
                align-items: center;
                border-bottom: 5px solid transparent;
                a{
                    text-decoration: none;
                    color: #000;

                }
                &:hover,
                &:focus{
                    border-bottom-color: $color_primary;
                    & a{
                        color: $color_primary;
                    }
                }
            }
        }
    }
}

</style>