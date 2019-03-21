<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <p class="big">Bursts</p>
            <p>of inspiration</p>
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
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        color: #ffffff;
        .big {
            font-size: 140px;
            font-family: 'Oswald', sans-serif;
            text-transform: uppercase;
        }
    }
}
</style>

