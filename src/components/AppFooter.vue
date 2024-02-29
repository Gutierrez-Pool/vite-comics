<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            links: [
                {
                    title: 'Dc Comics',
                    list: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    title: 'Shop',
                    list: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    title: 'DC',
                    list: [
                        'Terms Of Use',
                        'Privacy policy(New)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us'
                    ]
                },
                {
                    title: 'Sites',
                    list: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                }
            ],

            socialImages: [
                '/img/footer-facebook.png',
                '/img/footer-twitter.png',
                '/img/footer-youtube.png',
                '/img/footer-pinterest.png',
                '/img/footer-periscope.png'
            ],
        }
    },
}
</script>

<template>
    <footer>
        <div id="top-footer">
            <div v-for="linkList in links">
                <h3>
                    {{ linkList.title }}
                </h3>
                <ul>
                    <li v-for="currentLink in linkList.list">
                        {{ currentLink }}
                    </li>
                </ul>
            </div>
            <img src="/img/dc-logo-bg.png" alt="">
        </div>


        <div id="bottom-footer">
            <div class="btn">
                <a href="#">Sign-up now!</a>
            </div>
            <div id="socials">
                <span>Follow us</span>
                <div v-for="socialImage in socialImages">
                    <img :src="socialImage" alt="">
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
footer {
    color: white;

    #top-footer {
        display: flex;
        flex-flow: column wrap;
        align-content: flex-start;
        z-index: -2;

        position: relative;

        padding: 35px 15px;
        gap: 20px;


        height: 370px;
        // test
        background-image: url('/img/footer-bg.jpg');

        img {
            position: absolute;
            top: -100px;
            right: 0;
            z-index: -1;
        }

        h3 {
            text-transform: uppercase;
            padding-bottom: 15px;
        }

        ul {
            padding-right: 20px;
            list-style-type: none;

            li {
                font-size: small;
                color: #959595;
            }
        }
    }

    #bottom-footer {
        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 110px;

        padding: 30px 14px;
        background-color: #303030;

        .btn {
            padding: 17px 14px;
            border: 3px solid #0282f9;

            a {
                color: white;
                text-decoration: none;
                text-transform: uppercase;
                font-weight: bold;
            }
        }

        span {
            font-weight: bold;
            padding-right: 10px;
            text-transform: uppercase;
            color: #0282f9;
        }

        #socials {
            display: flex;
            align-items: center;

            gap: 20px;
        }

    }
}
</style>