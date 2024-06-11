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
      
    }
  }
}
</script>

<template>
       <article class="footer-nav-links">
            <div class="width-container-footer">
                <nav class="links-left">
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
       </article>
</template>


<style lang="scss" scoped>
    img {
        width: 100%;
    }

    .width-container-footer {
        max-width: 1200px;
        display: flex;
        padding: 0.25rem 0;
        margin-top: 2rem;
        margin: 0 auto;
    }

    .footer-nav-links {
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        display: flex;
        padding: 2rem;
        

        ul {
            flex-wrap: wrap;
        }

        li {
            padding: 0.25rem;

            a {
                color: #7c7d7f;
            }
        }

        h2{
            color: white;
            padding-bottom: 1rem;
            padding-top: 1.5rem;
            
        }
    }

    .links {
        margin-left: 1rem;
    }

    


</style>