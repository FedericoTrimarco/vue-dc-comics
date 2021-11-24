<template>
    <section id="footer_top">
        <div class="container-footer d-flex">
            
            <div class="dc-footer-list">
                <div class="list-left">
                    <ul>
                        <h2>DC COMICS</h2>
                        <li v-for="(link, index) in dcComicsLink" :key="`link-${index}`">
                            <a href="/">{{link.text}}</a>
                        </li>
                    </ul>
                    <ul>
                        <h2>SHOP</h2>
                        <li v-for="(link, index) in shopLink" :key="`link-${index}`">
                            <a href="/">{{link.text}}</a>
                        </li>
                    </ul>

                </div>
                <ul>
                    <h2>DC</h2>
                    <li v-for="(link, index) in dcLink" :key="`link-${index}`">
                        <a href="/">{{link.text}}</a>
                    </li>
                </ul>
                <ul>
                    <h2>SITES</h2>
                    <li v-for="(link, index) in sitesLink" :key="`link-${index}`">
                        <a href="/">{{link.text}}</a>
                    </li>
                </ul>
            
            </div>
            <div class="dc-footer-img text-end">
                <img src="@/assets/dc-logo-bg.png" alt="dc-logo">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterTop',
    data(){
        return{
            dcComicsLink: [
                {
                    text: 'Characters',
                    url: '/',
                },
                {
                    text: 'Comics',
                    url: '/',

                },
                {
                    text: 'Movies',
                    url: '/',

                },
                {
                    text: 'TV',
                    url: '/',

                },
                {
                    text: 'Games',
                    url: '/',

                },
                {
                    text: 'Videos',
                    url: '/',

                },
                {
                    text: 'News',
                    url: '/',

                },
            ],
            shopLink: [
                {
                    text: 'Shop DC',
                    url: '/',
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '/',
                },
            ],
            dcLink: [
                {
                    text: 'Terms of Use',
                    link: '/',
                },
                {
                    text: 'Privacy Policy (new)',
                    link: '/',
                },
                {
                    text: 'Ad Choices',
                    link: '/',
                },
                {
                    text: 'Advertising',
                    link: '/',
                },
                {
                    text: 'Jobs',
                    link: '/',
                },
                {
                    text: 'Subscription',
                    link: '/',
                },
                {
                    text: 'Talent Workshop',
                    link: '/',
                },
                {
                    text: 'CPSC Certificates',
                    link: '/',
                },
                {
                    text: 'Ratings',
                    link: '/',
                },
                {
                    text: 'Shop Help',
                    link: '/',
                },
                {
                    text: 'Contact Us',
                    link: '/',
                },
            ],
            sitesLink: [
                {
                    text:'DC',
                    url: '/',
                },
                {
                    text:'Mad Magazine',
                    url: '/',
                },
                {
                    text:'DC Kids',
                    url: '/',
                },
                {
                    text:'DC Universe',
                    url: '/',
                },
                {
                    text:'DC Power Visa',
                    url: '/',
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '@/styles/generals';
@import '@/styles/utilities';
section{
    display: flex;
    overflow: hidden;
    background-image: url('../assets/footer-bg.jpg');
    background-size: cover;
}
.dc-footer-list{
    width: 30%;
    display: flex;
    flex-wrap: wrap;
    ul{ 
        padding: 20px 0;
        margin-right: 50px;
        list-style: none;
        h2{
            font-size: 30px;
            margin-bottom: 15px;
            color: #fff;
        }
        li{
            margin-bottom: 10px;

            a{
                text-decoration: none;
                color: #989c9e;
                &:hover{
                    text-decoration: underline;
                }
            }
        }
    }
}
.dc-footer-img{
width: 70%;
img{
    width: 50%;
    position: relative;
    bottom: 50px;
}
}


</style>