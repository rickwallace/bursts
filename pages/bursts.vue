<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <ul>
                <li>
                    <nuxt-link to="/small_world">It's a Small World</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/avatar">Avatar</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/layers">Levels to This</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/perspective">Levels to This - Head On</nuxt-link>
                </li>
            </ul>
        </main>
    </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'

export default {
    components: {
        MyHeader
    }
}
</script>

<style lang="scss" scoped>
.container {
    background-color: #262626;
    min-height: 100vh;
    padding: 0 100px;
    header {
        display: flex;
        height: 70px;
        justify-content: flex-end;
        align-items: center;
        nav {
            ul {
                list-style: none;
                li {
                    display: inline;
                    a {
                        padding: 10px 20px;
                        font-family: 'Oswald', sans-serif;
                        color: #ffffff;
                        text-transform: uppercase;
                        text-decoration: none;
                    }
                }
            }
        }
    }
    main {
        min-height: calc(100vh - 90px);
        p {
            font-size: 40px;
            font-family: 'Oswald', sans-serif;
            color: #ffffff;
            text-transform: uppercase;
        }
        ul {
            margin: 0;
            margin-left: -20px;
            padding: 0;
            list-style: none;
            li {
                display: block;
                margin: 10px 0;
                a {
                    padding: 10px 20px;
                    font-family: 'Oswald', sans-serif;
                    color: #ffffff;
                    text-transform: uppercase;
                    text-decoration: none;
                }
            }
        }
    }
}
</style>

