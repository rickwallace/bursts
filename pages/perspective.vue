<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <div class="burst_info">
                <h1>Levels To It: Take Deux</h1>
                <table>
                    <tbody>
                        <tr>
                            <td>Location</td>
                            <td>Everyday life</td>
                        </tr>
                        <tr>
                            <td>Date</td>
                            <td>March 21, 2019</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="burst_container">                                
                <div class="circle">
                    <div class="phone">
                        <img class="base" src="@/assets/img/levelsTwo/iphone.png" alt="iPhone" />
                        <img class="code" src="@/assets/img/levelsTwo/code.png" alt="code" />
                        <img class="visual" src="@/assets/img/levelsTwo/visual.png" alt="visual" />
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
    perspective: 1000px;
    img {
        position: absolute;
        animation: 1.5s perspective 3.0s $easing forwards;
        // transform: rotateY(30deg) rotateX(50deg) rotateZ(-15deg);
        &.base {
            top: 0;
            left: 200px;
            margin-left: -97px;
        }
        &.code, &.visual {
            top: 41px;
            left: 118px;
        }
        &.base {
            animation: 1.5s perspective 3.0s $easing forwards, 3.5s wave 5.6s $easing infinite;
        }
        &.code {
            animation: 1.5s perspective 3.0s $easing forwards, 1.5s move-code 3.0s $easing forwards, 3.5s wave 5.3s $easing infinite;
        }
        &.visual { 
            animation: 1.5s perspective 3.0s $easing forwards, 1.5s move-visual 3.0s $easing forwards, 3.5s wave 5.0s $easing infinite;
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
    65% { transform: scale(0.9) }
    80% { transform: scale(1.0) }
    90% { transform: scale(0.95) }
    100% { transform: scale(1.0) }
}

@keyframes move-visual {
    0% { top: 41px; left: 118px; }
    100% { top: -7px; left: 113px; }
}

@keyframes move-code {
    0% { top: 41px; left: 118px; }
    100% { top: 25px; left: 113px; }
}

@keyframes wave {
    0% { transform: translateY(0) rotate3d(-8, -5, 6, -65deg) }
    50% { transform: translateY(-30px) rotate3d(-8, -5, 6, -65deg) }
    100% { transform: translateY(0) rotate3d(-8, -5, 6, -65deg) }
}

@keyframes perspective {
    0% {
        transform: rotateY(0) rotateX(0) rotateZ(0);
    }
    100% {
        transform: rotate3d(-8, -5, 6, -65deg);
    }
}
</style>

