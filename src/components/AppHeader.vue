<script>
export default {
  data() {
    return {
        navComics: [
            {
                id: 1,
                link: "CHARACTERS",
                active: false,
                url: '#'
            },
            {
                id: 2,
                link: "COMICS",
                active: true,
                url: '#'
            },
            {
                id: 3,
                link: "MOVIES",
                active: false,
                url: '#'
            },
            {
                id: 4,
                link: "TV",
                active: false,
                url: '#'
            },
            {
                id: 5,
                link: "GAMES",
                active: false,
                url: '#'
            },
            {
                id: 6,
                link: "COLLECTIBLES",
                active: false,
                url: '#'
            },
            {
                id: 7,
                link: "VIDEOS",
                active: false,
                url: '#'
            },
            {
                id: 8,
                link: "FANS",
                active: false,
                url: '#'
            },
            {
                id: 9,
                link: "NEWS",
                active: false,
                url: '#'
            },
            {
                id: 10,
                link: "SHOP",
                active: false,
                url: '#'
            },
        ]
      
    }
  }
}
</script>

<template>
    <div class="bg-color-page">
        <div class="width-container">
            <section class="logo">
                <img src="../assets/img/dc-logo.png" alt="comics-logo" class="main-dc-logo">
            </section>
    
            <section class="navbar">
                <nav>
                    <ul>
                        <li v-for="link in navComics" :key="link.id" :class="(link.active) ? 'active' : ' ' ">
                            <a href="">{{ link.link }}</a>
                        </li>
                    </ul>
                </nav>
            </section>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

div.bg-color-page {
    background-color: #ffffff;
}

.width-container {
    max-width: 1700px;
    display: flex;
    justify-content: space-around;
    margin: 0 auto;
}


img {
    width: 77%;
    padding-top: 1rem;
}

.navbar {
    display: flex;
    align-items: center;

    
    ul {
        display: flex;
        
        li {
            padding: 0.75rem;
            font-weight: 500;
            padding-top: 3rem;
            

            &.active {
                color: $active-link-color;
                border-bottom: 5px solid #517ef9;
                padding-bottom: 3.5rem;
                
            }
            
        }
    }
}



</style>