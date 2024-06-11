<script>
export default {
  data() {
    return {
        dcComicsLinks: [
            {
                id: 1,
                name: 'Charaters',
            },
            {
                id: 2,
                name: 'Comics',
            },
            {
                id: 3,
                name: 'Movies',
            },
            {
                id: 4,
                name: 'TV',
            },
            {
                id: 5,
                name: 'Games',
            },
            {
                id: 6,
                name: 'Videos',
            },
            {
                id: 7,
                name: 'News',
            },
        ],
        DcLinks: [
            {
                id: 1,
                name: 'Therms Of Use',
            },
            {
                id: 2,
                name: 'Privacy policy (New)',
            },
            {
                id: 3,
                name: 'Ad Choices',
            },
            {
                id: 4,
                name: 'Advertising',
            },
            {
                id: 5,
                name: 'Jobs',
            },
            {
                id: 6,
                name: 'Subscriptions',
            },
            {
                id: 7,
                name: 'Talent Workshop',
            },
            {
                id: 8,
                name: 'CPSC Certificates',
            },
            {
                id: 9,
                name: 'Ratings',
            },
            {
                id: 10,
                name: 'Shop Help',
            },
            {
                id: 11,
                name: 'Contact Us',
            },
        ],
        sitesLink: [
            {
                id: 1,
                name: 'DC',
            },
            {
                id: 2,
                name: 'MAD Magazine',
            },
            {
                id: 3,
                name: 'DC Kids',
            },
            {
                id: 4,
                name: 'DC Universe',
            },
            {
                id: 5,
                name: 'DC Power Visa',
            },
        ],
        shopLinks: [
            {
                id: 1,
                name: 'Shop DC',
            },
            {
                id: 2,
                name: 'Shop DC Collectibles',
            },
        ],
        socialsLinks: [
            {
                id: 1,
                img: "./src/assets/img/footer-facebook.png",
            },
            {
                id: 1,
                img: "./src/assets/img/footer-periscope.png",
            },
            {
                id: 1,
                img: "./src/assets/img/footer-pinterest.png",
            },
            {
                id: 1,
                img: "./src/assets/img/footer-twitter.png",
            },
            {
                id: 5,
                img: "./src/assets/img/footer-youtube.png",
            },
        ]
      
    }
  }
}
</script>

<template>
       <article class="footer-nav-links">
            <div class="width-container-footer">
                <div class="links-nav-container">
                    <nav class="links">
                        <h2>DC COMICS</h2>
                        <ul>
                            <li v-for="link in dcComicsLinks" :key="link.id">
                                <a href="">{{ link.name }}</a>
                            </li>
                            <h2>SHOP</h2>
                            <ul>
                                <li v-for="link in shopLinks" :key="link.id">
                                    <a href="">{{ link.name }}</a>
                                </li>
                            </ul>
                        </ul>
                    </nav>
                    <nav class="links">
                        <h2>DC</h2>
                        <ul>
                            <li v-for="link in DcLinks" :key="link.id">
                                <a href="">{{ link.name }}</a>
                            </li>
                        </ul>
                    </nav>
                    <nav class="links">
                        <h2>SITES</h2>
                        <ul>
                            <li v-for="link in sitesLink" :key="link.id">
                                <a href="">{{ link.name }}</a>
                            </li>
                        </ul>
                    </nav>
                </div>

                <div class="DC-image">
                </div>
            </div>
       </article>
       <article class="bg-footer-sign-links">
        <div class="footer">
            <section class="sign-up special-effect ">
                <button>SIGN-UP NOW!</button>
            </section>
            <section class="follow-socials">
                <h2>
                    FOLLOW US
                </h2>

                <div class="social-links " v-for="social in socialsLinks" :key="social.id">
                    <img :src="social.img" :alt="social.id">
                </div>
            </section>
        </div>

       </article>
</template>


<style lang="scss" scoped>
    img {
        width: 100%;
    }

    .follow-socials {
        display: flex;
        align-items: center;

        h2 {
            color: #0282f9;
        }

        div.social-links {
            margin-left: 1rem;

            img {
                width: 35px;

                &:hover {
                    background-color: #0282f9;
                    border-radius: 35px;
                    border: 1px solid white;
                }
            }

            
        }

    }

    button {
        background-color: #303030;
        border: 2px solid #0282f9;
        color: white;
        padding: 1rem 2rem;

        &:hover {
            background-color: #0282f9;
            border: 2px solid white;
        }
    }

    .bg-footer-sign-links {
        background-color: #303030;
        margin: 0 auto;
        padding: 2rem;
        position: relative;
        z-index: 2;

        .footer {
            display: flex;
            justify-content: space-around;
            max-width: 1900px;
            align-items: center;
            margin: 0 auto;
        }
    }



    div.DC-image {
        background-image: url(../assets/img/dc-logo-bg.png);
        width: 37%;
        height: 30rem;
        background-repeat: no-repeat;
        position: relative;
        bottom: 100px;
    }

    .links-nav-container {
        display: flex;
        padding: 0.25rem 0;
    }

    .width-container-footer {
        max-width: 1550px;
        display: flex;
        margin: 0 auto;
        justify-content: space-around;
    }

    .footer-nav-links {
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 21rem;
        overflow: hidden;
    
    }

    .links {
        margin-left: 1rem;

        ul {
            flex-wrap: wrap;
        }

        li {
            padding: 0.25rem;

            a {
                color: #7c7d7f;
                font-weight: 200;
            }
        }

        h2{
            color: white;
            padding-bottom: 1rem;
            padding-top: 1.5rem;
            
        }
    }

    


</style>