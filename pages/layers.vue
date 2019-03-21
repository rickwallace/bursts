<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <div class="burst_info">
                <h1>Levels To It</h1>
                <table>
                    <tbody>
                        <tr>
                            <td>Location</td>
                            <td>Everyday life</td>
                        </tr>
                        <tr>
                            <td>Date</td>
                            <td>March 20, 2019</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="burst_container">                                
                <div class="circle">
                    <div class="phone">
                        <img class="base" src="@/assets/img/levels/iphone.svg" alt="iPhone" />
                        <img class="code" src="@/assets/img/levels/code.svg" alt="code" />
                        <img class="visual" src="@/assets/img/levels/visual.svg" alt="visual" />
                    </div>
                </div>
            </div>
        </main>
    </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'

export default {
    components: {
        MyHeader
    },
    data: function () {
        return {
        };
    },
    methods: {}
}
</script>

<style lang="scss" scoped>
.container {
    background: url('~/assets/img/levels.png') no-repeat center center;
    background-size: cover;
    min-height: 100vh;
    padding: 0 100px;
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
    main {
        min-height: calc(100vh - 90px);
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        .burst_info {
            flex: 1;
            h1 {
                font-size: 40px;
                font-family: 'Oswald', sans-serif;
                color: #ffffff;
                text-transform: uppercase;
                margin-bottom: 10px;
            }
            table {
                color: #dddddd;
                font-size: 15px;
                font-family: 'Oswald', sans-serif;
                tbody {
                    tr {
                        td {
                            &:first-of-type {
                                color: #aaaaaa;
                                padding-right: 10px;
                            }
                        }
                    }
                }
            }
        }
        .burst_container {
            flex: 2;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 400px;
        }
    }
}

$radius: 400;
$easing: ease-in-out;

.circle {
    display: flex;
    align-items: center;
    justify-content: center;
    height: $radius * 1px;
    width: $radius * 1px;
    border-radius: 50%;
    background-color: rgba(#6b4242, 0.3);
    transform: scale(0);
    animation: 1.5s bounceIn 0.5s $easing forwards;
}

.phone {
    height: $radius * 1px;
    width: $radius * 1px;
    transform: scale(0);
    animation: 1.5s bounceIn 0.5s $easing forwards;
    img {
        position: absolute;
        &.base {
            top: 36px;
            left: -20px;
        }
        &.code, &.visual {
            top: 50px;
            left: 6px;
        }
        &.base {
            animation: 3.5s wave 3.6s $easing infinite; 
        }
        &.code {
            animation: 1.5s move-code 3.3s $easing forwards, 3.5s wave 3.3s $easing infinite; 
        }
        &.visual { 
            animation: 1.5s move-visual 3.0s $easing forwards, 3.5s wave 3.0s $easing infinite; 
        }

    }
}

@keyframes scaleIn {
    0% { transform: scale(0) }
    100% { transform: scale(1.0) }
}

@keyframes bounceIn {
    0% { transform: scale(0) }
    50% { transform: scale(1.0) }
    65% { transform: scale(0.8) }
    80% { transform: scale(1.0) }
    90% { transform: scale(0.95) }
    100% { transform: scale(1.0) }
}

@keyframes move-visual {
    0% { top: 50px }
    100% { top: -7px }
}

@keyframes move-code {
    0% { top: 50px }
    100% { top: 25px }
}

@keyframes wave {
    0% { transform: translateY(0) }
    50% { transform: translateY(-30px) }
    100% { transform: translateY(0) }
}
</style>

