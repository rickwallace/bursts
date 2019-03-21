<template>
    <header>
        <div class="logo">
            <nuxt-link to="/">
                <svg width="26px" height="23px" viewBox="0 0 26 23" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                    <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M23.6661001,11.3068 C25.0541733,9.358 24.9997117,7.0144 24.9997117,7.0144 C24.9997117,3.6936 22.3129381,1 18.9991576,1 C15.6867736,1 13,3.6936 13,7.0144 C13,3.6936 10.3132264,1 7.00084239,1 C3.6870619,1 1.00028833,3.6936 1.00028833,7.0144 C1.00028833,7.0144 0.945826704,9.358 2.33389995,11.3068 C3.72336965,13.2556 13,22 13,22 C13,22 22.2766304,13.2556 23.6661001,11.3068 Z" id="Shape" stroke="#FF4D4D" stroke-width="1.5" fill="#FF4D4D"></path>
                    </g>
                </svg>
            </nuxt-link>
        </div>
        <nav role="navigation">
            <ul>
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/bursts">Bursts</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<script>

export default {
    components: {
        
    }
}
</script>

<style lang="scss" scoped>
header {
    display: flex;
    height: 70px;
    align-items: center;
    nav {
        margin-left: auto;
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
</style>