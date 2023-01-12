<script>
export default {
    data() {
        return {
            footerLinks: [
                {
                    title: 'DC Comics',
                    links: [
                        'Characters', 'Comics', 'Movies', 'Tv', 'Games', 'Videos', 'News'
                    ]
                },
                {
                    title: 'Shop',
                    links: [
                        'Shop DC', 'Shop Dc Collections'
                    ]
                },
                {
                    title: 'DC',
                    links: [
                        'Terms Of use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops',
                        'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'
                    ]
                },
                {
                    title: 'Sites',
                    links: [
                        'DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'
                    ]
                },
            ],
        }
    },
}
</script>

<template>
    <footer>
        <section class="footer-top">
            <div class="my-container">
                <nav>
                    <div v-for="footerElement in footerLinks">
                        <h2>{{ footerElement.title }}</h2>
                        <ul>
                            <li v-for="footerLink in footerElement.links">{{ footerLink }}</li>
                        </ul>
                    </div>
                </nav>
            </div>
        </section>
        <section class="footer-bottom">
            <div class="my-container">
                <button>
                    Sign-up now!
                </button>
                <div>
                    <a href="#">Follow us</a>

                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

section.footer-top {
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;

    nav {
        display: flex;

        div {
            padding: 3rem 1rem;
        }
    }

    h2 {
        color: white;
        margin-bottom: 1rem;
        margin-right: 1rem;
        text-transform: uppercase;
    }

    li {
        color: $text-color;
        padding: .5rem 0;
    }
}

section.footer-bottom {
    background-color: #38332d;
    height: 150px;

    div.my-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;

        button {
            padding: .5rem;
            background-color: #38332d;
            color: white;
            border-color: $main-color;
            text-transform: uppercase;
            font-weight: bold;
        }

        a {
            text-transform: uppercase;
            text-decoration: none;
            color: $main-color;
            font-weight: bold;
        }
    }
}
</style>